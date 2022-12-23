# immunogenetr
An R library for HLA data functions

Version 0.1 - initial version
Notes: 
1. These functions rely heavily on REGEX patterns. I'm not completly convinced this is the best way to handle these functions.
2. Many of these functions have `across` within the function itself. I did this because it was easier to get the function working on multiple columns, but would it be better to have them more like traditional tidyverse functions, where `across` is applied outside of the function?
3. Many of these functions should have error messages, especially the functions for parsing GL strings. I have only written error functions for one of them so far.
4. Other functions needed:
	A. A GLstring_gene_separate function. Since genes are already separated in HML files, and this is primarily what I've been working with, I haven't needed it yet.
	B. A GLstring_parse function, which takes GL strings and separates them and keeps the first set of allleles at every locus. Essentially, this would be a wrapper for the other GL string functions, so you wouldn't have to call each every time you wanted to get the most likely typing out of a GL string.
	C. Matching grade functions. There are functions to identify mismatched alleles, but it would be useful to have functions to calculate matching scores (e.g. 8/8, 10/10, etc.).
