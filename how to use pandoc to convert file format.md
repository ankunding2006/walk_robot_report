The format of the input and output can be specified explicitly using command-line options. The input format can be specified using the -f/--from option, the output format using the -t/--to option. Thus, to convert hello.txt from Markdown to LaTeX, you could type:

pandoc -f markdown -t latex hello.txt
To convert hello.html from HTML to Markdown:

pandoc -f html -t markdown hello.html
Supported input and output formats are listed below under Options (see -f for input formats and -t for output formats). You can also use pandoc --list-input-formats and pandoc --list-output-formats to print lists of supported formats.

If the input or output format is not specified explicitly, pandoc will attempt to guess it from the extensions of the filenames. Thus, for example,

pandoc -o hello.tex hello.txt
will convert hello.txt from Markdown to LaTeX. If no output file is specified (so that output goes to stdout), or if the output file’s extension is unknown, the output format will default to HTML. If no input file is specified (so that input comes from stdin), or if the input files’ extensions are unknown, the input format will be assumed to be Markdown.
