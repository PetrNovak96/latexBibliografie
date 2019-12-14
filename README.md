# Jak udělat bibliografii v LaTEXu

1. vytvoř si v projektu nový soubor ```literatura.bib```
2. na vršek souboru ```main.tex``` přidej tento kód:
```TeX
%%% Nastavení pro použití samostatné bibliografické databáze.
\usepackage[
   backend=biber
 % ,style=iso-authoryear
  ,style=iso-numeric
  ,bibencoding=UTF8
  %,block=ragged
]{biblatex}
\let\cite\parencite
\bibliography{literatura}
```
3. do souboru ```literatura.bib``` si přidej tuhle citaci na zkoušku. Jak ty citace správně napsat, je dole.
```
@book{
   timtoSeOdkazuju,
   title =     {Cizinec hledá byt},
   author =    {Egon Hostovský},
   publisher = {Melantrich},
   isbn =      {1491958375,9781491958377},
   year =      {1947}
}   
```
5. někde na konci dokumentu urči, kde se seznam literatury vytiskne:
```TeX
\printbibliography[title={Seznam použité literatury},heading={bibintoc}]
```
6. na libovolném místě v textu použij citaci:
```TeX
\cite{timtoSeOdkazuju}
```
7. <kbd>Ctrl+S</kbd> pro zkompilování kódu. Měl by se potom objevit seznam použité literatury s jednou citací.