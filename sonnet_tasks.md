# Shakespeare's sonnets regex tasks

## simple tasks

- find all the roman numerals
- count the sonnets (dot matches all)
- find all lines that are not roman numerals
- find all non-blank lines
- find personal pronoun ‘I’ without finding roman numerals 
	- `egrep '.* .*' shakespeare-sonnets.txt | egrep --color '\bI\b'`

## slightly more complicated tasks
- find all enjambed lines and show lines before and after
	- `-C \w$`(all lines that do not end with punctuation)
	- if we pipe into a second operation, we can sort for only lines which contain spaces OR
	- with pcregrep: `\p{Ll}$` all lines that end in a lowercase letter (not punctuation and not roman numerals, fails for a line ending in ‘I’) OR
	- `.* .*\w$`

## rather difficult tasks (SERIOUSLY why would anyone want to do these???)
- count how many times each vowel occurs in the sonnets
	- `egrep -o '[aeiouy]' shakespeare-sonnets.txt | sort | uniq -c`	
- count how many times each character (case insensitive) occurs in the sonnets
	- `cat shakespeare-sonnets.txt | tr '[:upper:]' '[:lower:]' | egrep -o '.' | sort | uniq -c`
