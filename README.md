# Article Text Analysis for Sentiment Analysis
**Note: The _url link_ are not shown in the notebook due to copyright issues. Any url can be passed through the codes to extract the text and futher analyse.**

**Links to positive and negative word list:**

https://ptrckprry.com/course/ssd/data/negative-words.txt

https://ptrckprry.com/course/ssd/data/positive-words.txt
## Sentiment Analysis Parameters: </h2>
### 1. Positive Score: </h3>
This score is calculated by assigning the value of +1 for each word if found in the Positive Dictionary and then adding up all the values.
### 2. Negative Score: </h3>
This score is calculated by assigning the value of -1 for each word if found in the Negative Dictionary and then adding up all the values. We multiply the score with -1 so that the score is a positive number.
### 3. Polarity Score: </h3>
This is the score that determines if a given text is positive or negative in nature.<p>
It is calculated by using the formula:<p>
Polarity Score = (Positive Score – Negative Score)/ ((Positive Score + Negative Score) + 0.000001)<p>
Range is from -1 to +1<p>
### 4. Subjectivity Score: </h3>
This is the score that determines if a given text is objective or subjective. <p>
It is calculated by using the formula:<p>
Subjectivity Score = (Positive Score + Negative Score)/ ((Total Words after cleaning) + 0.000001)<p>
Range is from 0 to +1<p>


## Analysis of Readability
Analysis of Readability is calculated using the Gunning Fox index formula described below.
### 5. Average Sentence Length
Average Sentence Length = the number of words / the number of sentences
### 6. Percentage of Complex words 
Percentage of Complex words = the number of complex words / the number of words 
### 7. Fog Index
Fog Index = 0.4 * (Average Sentence Length + Percentage of Complex words)

### 8. Average Number of Words Per Sentence
The formula for calculating is:<p>
Average Number of Words Per Sentence = the total number of words / the total number of sentences

### 9. Complex Word Count
Complex words are words in the text that contain more than two syllables.

### 10. Word Count
We count the total cleaned words present in the text by 
1.	removing the stop words (using stopwords class of nltk package).
2.	removing any punctuations like ? ! , . from the word before counting.

### 11.	Syllable Count Per Word
We count the number of Syllables in each word of the text by counting the vowels present in each word. We also handle some exceptions like words ending with "es","ed" by not counting them as a syllable.

### 12. Personal Pronouns
To calculate Personal Pronouns mentioned in the text, we use regex to find the counts of the words - “I,” “we,” “my,” “ours,” and “us”. Special care is taken so that the country name US is not included in the list.

### 13.	Average Word Length
Average Word Length is calculated by the formula:<p>
Sum of the total number of characters in each word/Total number of words

## Sentiment Analysis Machine Learning Model
The above parameters are used for modelling, but ML is not included in the current CodeBook.
