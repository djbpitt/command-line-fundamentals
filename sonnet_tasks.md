# Shakespeare’s sonnets regex tasks

## Simple tasks

- Find all the roman numerals
- Count the sonnets (dot matches all)
- Find all lines that are not roman numerals
- Find all non-blank lines
- Find personal pronoun ‘I’ without finding roman numerals 
	- `egrep '.* .*' shakespeare-sonnets.txt | egrep --color '\bI\b'`

## Slightly more complicated tasks
- Find all enjambed lines and show lines before and after
	- `-C \w$`(all lines that do not end with punctuation)
	- If we pipe into a second operation, we can sort for only lines which contain spaces OR
	- With `pcregrep`: `\p{Ll}$` all lines that end in a lowercase letter (not punctuation and not roman numerals, fails for a line ending in ‘I’) or
	- `.* .*\w$`

## Rather difficult tasks (*seriously* why would anyone want to do these???)
- Count how many times each vowel occurs in the sonnets
	- `egrep -o '[aeiouy]' shakespeare-sonnets.txt | sort | uniq -c`	
- Count how many times each character (case insensitive) occurs in the sonnets
	- `cat shakespeare-sonnets.txt | tr '[:upper:]' '[:lower:]' | egrep -o '.' | sort | uniq -c`
