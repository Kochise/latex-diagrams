# latex-diagrams
LaTeX package to interface with diagrams (npm)

Source : https://github.com/Kochise/latex-diagrams

## installation

Get 'nvm' for Windows : https://github.com/coreybutler/nvm-windows/releases
Uncompress/install it where you need.

	\>cd nvm
	\nvm>nvm install 12.17.0
	\nvm>nvm use 12.17.0
	\nvm>node -v
	v12.17.0
	\nvm>npm install -g diagrams

	xcopy /c /h /e /r /q /y latex-diagrams <miktex>\texmfs\install\tex\latex\diagrams
	start "" "<miktex>\miktex-portable.cmd"
	Refresh the filename database.
	Update the package database.

You should be ready to go.

Alternatively, you can use https://github.com/Kochise/win_portable

## usage

See https://github.com/francoislaberge/diagrams
See also https://github.com/adrai/flowchart.js

In your preamble :

	\def\imagepath{./images}
	\graphicspath{{\imagepath/}}
	\usepackage[imagepath=\imagepath]{diagrams}

In your document :

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

## limitations

All parameters, but width, are mandatory.
Do not duplicate refname (for obvious reason).

## greetings

Based on https://github.com/dakusui/latex-ditaa
Also interested into https://github.com/sile-typesetter/sile
