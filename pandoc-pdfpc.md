% Vorträge mit Pandoc und pdfpc
% Paul Menzel (Max-Planck-Institut für molekulare Genetik)
% 19. September 2019

# Werkzeuge

1.  [Pandoc](https://pandoc.org/) ist ein freier Parser für Multidokumentenformate.
1.  Basis: erweitertes Markdown, z.\ B. für Tabellen
1.  git
1.  Vorträge: Markdown → LaTeX/Beamer → PDF
    1.  LaTeX viel Boilerplate
1.  [pdfpc](https://pdfpc.github.io/): PDF presenter console with multi-monitor support

::: notes

1.  Informationen wichtig
1.  Animationen nur selten sinnvoll

:::

# Beispiel: Textdatei

    $ vim test.md
    $ git init
    $ git add test.md
    $ git commit -a

# Beispiel: Umwandlung mit Pandoc

    $ pandoc -s -t beamer -V aspectratio=169 -o test.pdf test.md

XeLaTeX

    $ pandoc -s -t beamer --pdf-engine=xelatex -V aspectratio=1610 \
      -o test.pdf test.md

# Beispiel: Präsentation von PDF-Datei

1.  Standard-PDF-Anzeigeprogramme ohne Multi-Monitor-Unterstützung
    1.  Anzeige der nächsten Folie
    1.  abgelaufene Zeit, Restzeit
1.  bekannt aus LibreOffice Impress, reveal.js, …
1.  GNU/Linux, Microsoft Windows 10 (Windows Subsystem for Linux), macOS: https://github.com/pdfpc/pdfpc#installation

    $ pdfpc test.pdf

# Beispiel: pdfpc-Dokumentation

1.  https://github.com/pdfpc/pdfpc/releases/download/v4.3.0/pdfpc-demo.pdf
1.  https://github.com/pdfpc/pdfpc/releases/download/v4.3.0/pdfpc-video-example.zip

# Nachteile/offene Fragen

1.  Einbinden von Bilder
1.  Animationen
1.  LaTeX-Kommandos
    1.  Umwandeln von Markdown in TeX und diese Datei weiterverarbeiten
