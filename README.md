# latex-diagrams
LaTeX package to interface with diagrams (npm)

Source : https://github.com/Kochise/latex-diagrams

## installation

Get 'nvm' for Windows : https://github.com/coreybutler/nvm-windows/releases<br>
Uncompress/install it where you need.<br>

```batch
\>cd nvm
\nvm>nvm install 12.17.0
\nvm>nvm use 12.17.0
\nvm>node -v
v12.17.0
\nvm>npm install -g diagrams

xcopy /c /h /e /r /q /y latex-diagrams <miktex>\texmfs\install\tex\latex\diagrams
start "" "<miktex>\miktex-portable.cmd"
```

Refresh the filename database.<br>
Update the package database.<br>
You should be ready to go.<br>

Alternatively, you can use https://github.com/Kochise/win_portable

## usage

See https://github.com/francoislaberge/diagrams<br>
See also https://github.com/adrai/flowchart.js<br>

In your preamble :

```latex
\def\imagepath{./images}
\graphicspath{{\imagepath/}}
\usepackage[imagepath=\imagepath]{diagrams}
```

In your document :

```latex
%\begin{diagrams}[width]{type}{caption}{refname} with type=flowchart/sequence/dot/railroad
\begin{diagrams}[4cm]{flowchart}{diagrams caption example}{diagramsexample}
st=>start: Start
e=>end
op1=>operation: My Operation
sub1=>subroutine: My Subroutine
cond=>condition: Yes
or No?:>http://www.google.com
io=>inputoutput: catch something
st->op1->cond
cond(yes)->io->e
cond(no)->sub1(right)->op1
\end{diagrams}
```

## options

Not much available, beside the type selection.

## limitations

All parameters, but width, are mandatory.<br>
Do not duplicate refname (for obvious reason).<br>

## greetings

Based on https://github.com/dakusui/latex-ditaa<br>
Also interested into https://github.com/sile-typesetter/sile<br>
