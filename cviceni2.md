## Nastavení dokumnetu
```latex
\documentclass[12pt,a4paper]{report}
```

nastaví velikost fontu, papíru a styl dokumentu

### Vygenerování titulní stránky
```latex
\begin{document} 
\author{Pavel Máca}
\title{Tiulek}
\date{\today}
\maketitle
\newpage
```

## Dělení slov
Nastavení pro celý dokument
```latex
\hyphenation{knihov-na knihov-ny}
```

Uvnitř dokumentu (pokud latex nedělí slovo správně, nebo víme že použijeme jednou)

```latex
Byl jsem tlumo\-čit v knihov\-ně.
```


Pokud chceme, aby  se některé slovo nedělilo, nastavíme ho celé bez dělené v `\hyphenation`

## Číslování stránek
```latex
\pagestyle{styl}

```

- empty = žádné
- plain - dole uprostřed (výchozí)
- headings - v pravo nahoře
- myheadings - možnost modifikace

Je možné modifikovat jednotlivé stránky.
Stačí napsat znovu \pagestyle{none} na stránce, kde nechceme mít např. číslování.

## Řádkování
### Zalovení řádku v odstavci - `\\`

### Odstavec bez zalomení na konci
Před odstavec vložit `\noindent`

### Nedělitelná mezera 
Místo mezery se zapíše `~`.
Například za  `šel jsem k~bazenu`


## Zápis speciálních znaků
```latex
\ = $\backslash$
~ = $\sim$
# = \#
% = \%
```

Další možnost je použít `\verb@...@`
Všechny znaky mezi zavináči jsou brány jako obyčejný text.
Místo zavináčů lze použít jakýkoli znak (ideálně speciální)
```latex
\verb%@%
\verb@%@
```

## Nadpisy
`\chapter{Super nadpis}`  
`\chapter*{Super nadpis}` - nadpis bez číslování

```latex
\chapter{Lorem}
\section{nadpis s číslováním}
\subsection{nadpis bez číslování}
\subsubsection{podnadpis druhé úrovně}
```

## Vygenerování obsahu `\tableofcontents`
Nutné dva průchody

## Přílohy
```latex
\appendix
\chapter{Seznam}
\section{Materiál}
Písek, cemnt, voda
\section{Nářadí}
Míchačka, lopata, kolečko
```
