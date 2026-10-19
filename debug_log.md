# debug_log.md
# Author: [Molly Audet]

## Bug 1
Error Type: KeyError 
File + Line: week8_buggy.py and Line 13
What the error means: The error indicates that the dictionary key does not exist, and may be from either a typo in a key name, or wrong capitalisation. 
What I told the duck: The goal of the script is to retrieve the records, the designated total, and set limit to then print a short summary of the two and identifying if that total is over the set limit. Records are defined in a dictionaries from line 4-6, def functions for retrieving total is line 10-14, set limit is 16-17, and format summary line 19-20, and finally the print statement in 23 and 24. Since we have a typo that occurs at the dictionaries in the first record with taylor and 'amout', when it retrieves what is meant to be 'amount' in line 13, it fails to do so because of the typo.
What I tried: I began from line 13 and worked upward to line 1, checking the key names against what it asks for. Once I checked the records, I identified the error in the first record with 'Taylor' and 'amout'
How I fixed it: I added a debug statement within the def function for get_total in order to identify the keyerror within the records. Once it identified the 'amout' and 'amount' typo between the records, I fixed the typo and removed the statement. Finally, running it once more to confirm the bug was gone.


## Bug 2
Error Type: TypeError
File + Line: week8_buggy.py and Line 17
What the error means: The error indicates that the wrong type was used in an operation, making it non-callable, this occurs when '>' cant compare an int to a str.
What I told the duck: The goal of line 17 is to compare the amount to 100 and return whether it's over. When evaluating line 17, the type error is seen through the use of '>' between an int 'amount' and the str '1000.' To solve that, we will need to convert '1000' into a int to be properly read.
What I tried: I began from line 17 and identified the 'int' and 'str' issue occuring due to '1000' when 1000 is meant to be a int to be read through the script. 
How I fixed it: I removed the '1000' to make it 1000 from a str to an int, ran the script to see the ouput ending in 'True', and confirmed the bug was gone.

## After Fixing Both Bugs
Final Output: The script prints 'Total: $5150.00 across 3 records True'
Did pytest pass? Yes, each of the 13 test files (8 from lab 7 and 5 from lab 8) residing in tests passed.

## AI Literacy Reflection
Did I use AI? Yes
If yes -- explain exact prompt I used: You are a Python Developer. Assist me in my understanding of debugging a python script in VSCode using the first two steps of the traceback method: Step 1: Read the traceback — bottom-up. Note the error type, file, and line number. Step 2: Write your hypothesis — what you think is wrong, in your own words, BEFORE touching any code. (Explain it to the duck.). I will provide my understanding and then you will assess it and push me in the right direction. | S1: The traceback indicates that the first error, a keyerror, is within line 13 and week8_buggy.py. S2: What I think is wrong is what happens with a key error, which is what occurs when a dictionary key does not exist due to a typo in a key name. Since its in line 13 or the total line, I think the amount error is due to the specific key 'amount'
What AI explained: AI would then identify what is correct in my own understanding, and give me helpful pointers in building on my own understanding in the code and identifying the proper terminology when creating entries.
What I changed myself: I chose to write my own duck and hypothesis entries in my own words, and I corrected the error in Bug 2 myself.
Can I explain every fixed line? Yes

## What I learned
Through this week's lab, I learned the importance in knowing the proper steps to debugging and utilizing AI as a helpful tool, but not an entire substitute to learning how to fix debugging issues. For example, I learned how to properly read a traceback error and use the duck technique to identify where the issue is. A useful resource in identifying any complications in code, but understanding the basics yourself and using AI to double-check your reasoning and terminology used is necessary to truly learn.

