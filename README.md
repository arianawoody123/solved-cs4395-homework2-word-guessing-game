Download Link: https://assignmentchef.com/product/solved-cs4395-homework2-word-guessing-game
<br>
<strong>Objective:</strong> Use Python and NLTK features to explore a text file and create a word guessing game

<strong>Turn in:</strong>  your Python .py file (Do not turn in a Jupyter notebook)

<ol>

 <li>Download the anat19.txt file from Piazza and save it in the same folder as your Python program. The file is the text from one chapter of an anatomy textbook. Send the filename to the main program in a system argument. If no system arg is present, print an error message and exit the program.</li>

 <li>Read the input file as raw text. Calculate the lexical diversity of the tokenized text and output it, formatted to 2 decimal places. Lexical diversity is the number of unique tokens divided by the total number of tokens. Lexical diversity indicates the richness of vocabulary in a text. For example, a lexical diversity of 0.05 means that 5% of the words in a text are unique.</li>

 <li>Write a function to preprocess the raw text:

  <ol>

   <li>tokenize the lower-case raw text, reduce the tokens to only those that are alpha, not in the NLTK stopword list, and have length &gt; 5</li>

   <li>lemmatize the <u>tokens</u> and use set() to make a list of unique lemmas</li>

   <li>do pos tagging on the unique lemmas and print the first 20 tagged items (see the pos_NLTK notebook in Part 2 of the GitHub)</li>

   <li>create a list of only those lemmas that are <u>nouns</u></li>

   <li>print the number of tokens (from step a) and the number of nouns (step d)</li>

   <li>return <u>tokens</u> (not unique tokens) from step a and <u>nouns</u> from the function</li>

  </ol></li>

 <li>Make a dictionary of {noun:count of noun in tokens} items from the nouns and tokens lists; sort the dict by count and print the 50 most common words and their counts. Save these words to a list because they will be used in the guessing game.</li>

 <li>Make a guessing game function:

  <ol>

   <li>give the user 5 points to start with; the game ends when their total score is negative, or they guess ‘!’ as a letter</li>

   <li>randomly choose one of the 50 words in the top 50 list (See the random numbers notebook in the Xtras folder of the GitHub)</li>

   <li>output to console an underscore _ for each letter in the word</li>

   <li>ask the user for a letter</li>

   <li>if the letter is in the word, print ‘Right!’, fill in all matching letter _ with the letter and add 1 point to their score</li>

   <li>if the letter is not in the word, subtract 1 from their score, print ‘Sorry, guess again’</li>

   <li>guessing for a word ends if the user guesses the word or has a negative score</li>

   <li>keep a cumulative total score and end the game if it is negative (or the user entered ‘!’) for a guess</li>

   <li>right or wrong, give user feedback on their score for this word after each guess</li>

  </ol></li>

</ol>