# quoteography
Reference quotes as you would cite bibliographic sources. 
Quotes are numbered in the order they are referenced (cited), and a table of quotes is printed at the end. 

## Usage
### Defining quotes
First, prepare the "quote-file", containing the quotes you wish to cite as a list of quotes and matching quote keys:
```
\defineQuote{quoteKey}{Blah-blah quote.}
\defineQuote{barbaz}{Quote regarding the subject of bar and baz.}
```
It is similar in its role the `.bib` and `.bbl` files together; given the simple syntax, there is no reason for more advanced mechanics (for now at least). 
This simple syntax makes it easy to generate, e.g. from a CSV file.

### Referencing quotes
Then, in your document, use `\refQuote{quoteKey}`, in the same way that you would use `\cite{citationKey}`. 
This will insert a number (e.g., `〈1〉`) and a reference to the actual quote in the quote table. 

The quote table has to be generated at the end of the document, by calling `\quoteography{quotes.tex}`. 
As for bibliographies, this package needs two runs in order to build the references. 
Only referenced quotes will be included. 

**Don't forget to import the package: `\usepackage{quoteography}`.**

## Customization and contributions
The code is commented and interesting modification points, notably regarding [appearance](https://github.com/perfaram/quoteography/blob/main/quoteography.sty#L14), are fairly simple. 
Given the permissive licensing, we encourage you to tinker with it. 
If your only changes are appearance-related, please do not submit PRs. 
However, if you add features (such as support for citation author or other metadata system, quote-file generation capabilities, options to change citation numbering), or of course fix a bug, please submit a PR. 