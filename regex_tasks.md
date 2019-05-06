# *enable1.txt* regex activities

## Beginner tasks

- Does this list contain hyphens or apostrophes?
- Does this list contain one-letter words?
- Words that contain “fruit”
- Words that begin with “x”
- Words that end with “x”
- Words that begin and end with “x”
- Words that contain two consecutive “k”s
- Words following the ‘un-’, ‘-less’, and ‘un...less’ patterns
- Words that begin with “x” or “q”
- Words that begin with “ex” or “eq”
- Words of a certain length 

## Slightly more complicated tasks
- Words that begin and end with the same letter
- Words that begin and end with the same vowel
- Words that begin/contain/end with two consecutive same letters
- Words that begin with ‘un’ or ‘non’
- Words that begin with two consecutive same letters and end with two consecutive same letters 
- Words that contain only letters from the first half of the alphabet
- Words that contain ‘q’ not followed by ‘u’
- Words that begin with ‘q’ not followed by ‘u’ 
	- `pcregrep --color 'q(?!u)' enable1.txt`
- Words that don't contain an ‘e’
- Words that contain no vowels
- Words with five consecutive vowels
- Reduplicated words
- Words that begin with seven consonants
- All words with three ‘z’s (then try using a variable)
- Palindromes (specific sizes)
- Words of a certain minimum length
- Words of a certain maximum length
- Words between certain lengths

## Tasks that require pipes (`|`)
- Words that contain all five vowels
- Words with two or more vowels in a row AND more than five letters


## `egrep`switches
- `-C`: words with two consecutive ‘z’s along with the words before and after them
- `-c`: count
- `-n`: line number
- `-v`: lines that do not match the regex
- `-l`: names of files that contain the matched string
- `-L`: names of files that don't contain the matched string
- `-i`: case insensitive
- `-o`: print only matching string
- `-m number`: print only a certain number of results
- `-w`: match only whole words
