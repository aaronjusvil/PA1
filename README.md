Aaron Justine V. Sanga 2ECE-A
# PA1 - Introduction to Python Programming
In this Programming Assignment, we are asked to use and apply the basic functions and codes of python programming in different situations. 

**1. Alphabet Soup**
**Problem:**
Create a function that takes a string and returns a string with its letters in alphabetical order.

**Code Description:**
In the code, a function aphabet_soup is created, that takes an input from the user, organizes the letters from highest to lowest based on their ASCII values in the form of a list. Then, the elements of that list are joined together to create a new string

```
#Defining the function
def alphabet_soup(x):
    return(''.join(sorted(x))) 
    #When word 'x' is defined by user input, the letters are separated, sorted, and joined together again by connector '', then returned

#User inputs a word
Word = input("Input word: ")

#The inputted word is put in the alphabet soup function as 'x', sorting it and assigning it to another variable
Sorted_word = alphabet_soup(Word)

#Prints the alphabetized word
print("Sorted word: ", Sorted_word)
```

**Output:**
```
Input: alphabet
Output: aabehlpt
```
-----------------------------------------------------------------------------------
**2. Emotify**
**Problem:**
Create a function that changes specific words into emoticons. Given a sentence as a string, replace the words smile, grin, sad and mad with their corresponding emoticon:

**Code Description:**
In the code, the function emotify takes a string input from the user, and looks for the words 'smile', 'grin', 'sad', or 'mad' in that string. If it finds one or more of those words in the string, they are replaced with their respective emoticon

```
#Defining the function
def emotify(y):
    y=y.replace("smile", ":)")
    y=y.replace("grin", ":D")
    y=y.replace("sad", ":(")
    y=y.replace("mad", ">:(")
    #If there are the words "Smile", "grin", "sad", "mad" in the sentence 'y', a new sentence is created transforming those words into emoticons
    #That new sentence is then assigned to 'y'
    return(y)

#Ask users to input a sentence
Sentence = input("Input sentence: ")

#Emotify the sentence using the function and assign it to another variable
Emotified_sentence = emotify(Sentence)
#Print the emotified sentence

print("Emotified Sentence: ", Emotified_sentence)
```

**Output:**
```
Input: I'm so mad
Output: I'm so >:(
```
-----------------------------------------------------------------------------------
**3. Unpacking List**
**Problem:** Unpack the list writeyourcodehere into three variables, being first, middle, and last, with middle being everything in between the first and last element. Then print all three variables.

**Code Description:**
In the code, the user is asked to input a list, a set of numbers separated by spaces. The program turns that into an actual python list, and the first, middle, and last elements of that list are displayed, if the number of elements is sufficient. The middle presents all numbers between the first and last element.

```
#Ask users to input a set of numbers separated by spaces
List = input("Enter numbers with spaces in between: ")

#Splits the set into individual strings, turning it into a list
Newlist = List.split()

#The list has to have 3 or more digits, in order to have a first, middle, and last
if len(Newlist) >=3:
     first, *middle, last = Newlist #unpacks the list into three. First takes the first digit, and last takes the last, middle takes everything in between
     print ("first: ", first, "\tmiddle: ", middle, "\tlast: ", last)#prints all parts side by side, separated and labeled
else:
     print("Input 3 or more digits")#if the inputted list does not have 3 or more digits, an error message will appear
```

**Output:**
```
Input: 1 2 3 4 5 6 7 8 9 10
Output: first:  1 	middle:  ['2', '3', '4', '5', '6', '7', '8', '9'] 	last:  10
```
