## Nice beamer themes for Latex

- [Ocean (mine 🐧)](https://raw.githubusercontent.com/ngntrgduc/ocean-beamer-theme/master/ocean.pdf)

- Antibes ![beamer-default-Antibes-1.png (1024×768) (hartwork.org)](https://hartwork.org/beamer-theme-matrix/all/beamer-default-Antibes-1.png)

- Berkeley ![beamer-default-Berkeley-1.png (1024×768) (hartwork.org)](https://hartwork.org/beamer-theme-matrix/all/beamer-default-Berkeley-1.png)

- CambridgeUS ![beamer-default-CambridgeUS-1.png (1024×768) (hartwork.org)](https://hartwork.org/beamer-theme-matrix/all/beamer-default-CambridgeUS-1.png)

- Madrid ![beamer-default-Madrid-1.png (1024×768) (hartwork.org)](https://hartwork.org/beamer-theme-matrix/all/beamer-default-Madrid-1.png)

- Warsaw ![beamer-default-Warsaw-1.png (1024×768) (hartwork.org)](https://hartwork.org/beamer-theme-matrix/all/beamer-default-Warsaw-1.png)

## Matrix
### How to left-align entries in a matrix
- `\begin{matrix*} [〈col〉] 〈contents〉 \end{matrix*}`: simple matrix,
- `\begin{pmatrix*}[〈col〉] 〈contents〉 \end{pmatrix*}`: matrix surrounded by matching parenthesis,
- `\begin{bmatrix*}[〈col〉] 〈contents〉 \end{bmatrix*}`: matrix surrounded by matching square brackets,
- `\begin{Bmatrix*}[〈col〉] 〈contents〉 \end{Bmatrix*}`: matrix surrounded by matching curly brackets (braces),
- `\begin{vmatrix*}[〈col〉] 〈contents〉 \end{vmatrix*}`: matrix surrounded by matching vertical lines (like for determinant),
- `\begin{Vmatrix*}[〈col〉] 〈contents〉 \end{Vmatrix*}`: matrix surrounded by matching double vertical lines.

The `<col>` optional argument specifies the column alignment, and should be `c`, `l` or `r` for centered (default), left-aligned and right-aligned, respectively.

## Latex builtin color
![](https://latex-beamer.com/wp-content/uploads/2021/08/Base-Colors-Latex-Beamer.webp)

## Define custom colors
In general, the command to define a color is:
```tex
\definecolor{name}{model}{color definition}
```
where name is the name which will take the color, model is the model used
to define it and color definition is the definition according to the selected
model. The most common color models and their definition syntax are the
following:

- `rgb`: Is specified as three comma-separated values between 0 and 1 that represent the amount of red, green and blue (in this order) that the color has.
- `RGB`: The same as before but with the values going between 0 and 255.
- `HTML`: Consists of 6 hexadecimal digits that represent the color in HTML code.

The most practical is using the command:
```tex
\colorlet{name}{combination}
```
where name is the name of the new color and combination is a combination of preexisting colors. The percentage of every color in the combination is written between ! signs. For instance:
```tex
\colorlet{ochre}{blue!20!yellow!80!}
```

## Higlight text
```tex
\colorbox{color}{text}
```
## Have slide numbering in Warsaw theme 
```tex
\setbeamertemplate{page number in head/foot}[totalframenumber]
```

## [Underline the right way](https://alexwlchan.net/2017/latex-underlines/)
