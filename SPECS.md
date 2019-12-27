# Specs

## First word of every line is parsed for `.` and `#` characters followed by an html-conforming character / a not-space character and then rendered by pug

`.cat` -> `<div class=“cat”>`  
`#dog` -> `<div id=“dog”>`  
`span.bff#dog` -> `<span class="bff" id=“dog”>`

⚠️ Valid Markdown like `# A Markdown headline` still needs to render as a standard markdown headline
