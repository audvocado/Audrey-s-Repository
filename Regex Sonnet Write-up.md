# Regex Sonnet Write-up

Step 1. We need to start by deleting the leading spaces. Use ^+ to do so. 
By using the "caret" ^, you ensure the regex only looks at the very start 
of each line, leaving the spaces between words untouched. And + is used
to indicate one or more. 
Step 2. Start by tagging every line. In the find box put space+ and in the 
replace box enter use the <line></line> mark up this will create a capture 
group when you put \0 inside. 
Step 3. Next you have to change the Roman numerals so that they are no longer
included in the line markup. In the find box put <line>([IVXLC]+)</line> and
in the replace box put <sonnet number="\1">. 
Step 4. Do some final clean ups. Making sure you have an open and closing root.
That all your sonnets have their closing roots. Fix the title and author by
giving them a markup. And should be finished. 