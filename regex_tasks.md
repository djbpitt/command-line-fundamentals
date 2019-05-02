# *enable1.txt* regex activities

## beginner tasks

- does this list contain hyphens or apostrophes?
- does this list contain one-letter words?
- words that contain “fruit”
- words that begin with “x”
- words that end with “x”
- words that begin and end with “x”
- words that contain two consecutive “k”s
- words following the ‘un-’, ‘-less’, and ‘un...less’ patterns
- words that begin with “x” or “q”
- words that begin with “ex” or “eq”
- words of a certain length 

## slightly more complicated tasks
- words that begin and end with the same letter
- words that begin and end with the same vowel
- words that begin/contain/end with two consecutive same letters
- words that begin with ‘un’ or ‘non’
- words that begin with two consecutive same letters and end with two consecutive same letters 
- words that contain only letters from the first half of the alphabet
- words that contain ‘q’ not followed by ‘u’
- words that begin with ‘q’ not followed by ‘u’ 
	- `pcregrep --color 'q(?!u)' enable1.txt`
- words that don't contain an ‘e’
- words that contain no vowels
- words with five consecutive vowels
- reduplicated words
- words that begin with seven consonants
- all words with three ‘z’s (then try using a variable)
- palindromes (specific sizes)
- words of a certain minimum length
- words of a certain maximum length
- words between certain lengths

## tasks that require pipes “|”
- words that contain all five vowels
- words with two or more vowels in a row AND more than five letters


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
