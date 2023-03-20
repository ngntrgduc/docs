# How to left-align entries in a matrix
- `\begin{matrix*} [〈col〉] 〈contents〉 \end{matrix*}`: simple matrix,
- `\begin{pmatrix*}[〈col〉] 〈contents〉 \end{pmatrix*}`: matrix surrounded by matching parenthesis,
- `\begin{bmatrix*}[〈col〉] 〈contents〉 \end{bmatrix*}`: matrix surrounded by matching square brackets,
- `\begin{Bmatrix*}[〈col〉] 〈contents〉 \end{Bmatrix*}`: matrix surrounded by matching curly brackets (braces),
- `\begin{vmatrix*}[〈col〉] 〈contents〉 \end{vmatrix*}`: matrix surrounded by matching vertical lines (like for determinant),
- `\begin{Vmatrix*}[〈col〉] 〈contents〉 \end{Vmatrix*}`: matrix surrounded by matching double vertical lines.

The `<col>` optional argument specifies the column alignment, and should be `c`, `l` or `r` for centered (default), left-aligned and right-aligned, respectively.
