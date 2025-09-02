Aaron Justine V. Sanga 2ECE-A
# PA1 - Introduction to Python Programming
In this Programming Assignment, we are asked to use and apply the basic functions and codes of python programming in different situations. 

**1. Alphabet Soup**
**Problem:**
Create a function that takes a string and returns a string with its letters in alphabetical order.

**Code Description:**
This code displays how to use the ```sorted()``` and ```.join()``` functions to convert a string into a list of sorted individual elements, and then joined together by a connector, in this case, ```''.join()``` is used so that the output is a string without spaces. The user is asked to input a string, and that string is inserted to the function under a different variable. The code below has comments that explain how every line works, and what they do for the final output

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

**How to Get Started:**
```
Input: alphabet
Output: aabehlpt
```
-----------------------------------------------------------------------------------
**2. Emotify**
**Problem:**
Create a function that changes specific words into emoticons. Given a sentence as a string, replace the words smile, grin, sad and mad with their corresponding emoticon:

**Code Description:**
This code displays how a function can detect certain words in an inputted string, and replace them with another string using the ```replace()``` function. For example, the code ```y=y.replace("smile", ":)")``` works so that if the word smile is found in the inputted string, it gets replaced with a smiling emoji. It shows how strings can be modified with the help of reassigning of variables, without changing the whole string. The user is asked to input a string, and that string is inserted into the function under another variable. The code below has comments that explain how every line works, and what they do for the final output

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

**How to Get Started:**
```
Input: I'm so mad
Output: I'm so >:(
```
-----------------------------------------------------------------------------------
**3. Unpacking List**
**Problem:** Unpack the list writeyourcodehere into three variables, being first, middle, and last, with middle being everything in between the first and last element. Then print all three variables.

**Code Description:**
This code shows how an inputted set of numbers as a string can be split into a list of individual strings using ```.split()```. This code also shows how the if else syntax works, and finally, shows the usefullness of unpacking a list when we try to locate and extract specific variables from a list. The user is first asked to input a set separated by spaces. That list is then split using ```.split()```, and that splitted list is assigned under a new name ```Newlist```. The if else statement in the code requires the list to have 3 or more elements in order to have a first, middle, and last. If the condition is satisfied, the first, middle, and last are printed, and if not, then the user will recieve an error saying that they need to input 3 or more numbers. The code below contains comments that explain how every line works.

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

**How to Get Started:**
```
Input: 1 2 3 4 5 6 7 8 9 10
Output: first:  1 	middle:  ['2', '3', '4', '5', '6', '7', '8', '9'] 	last:  10
```
