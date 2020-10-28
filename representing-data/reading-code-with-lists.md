# Reading Code With Lists

## Introduction

Lists are a data type. Also, lists are a **data structure** that organizes many kinds of data into an ordered list.

As programmers, we want to have the skills to efficiently and elegantly use lists while we work with data. We should get comfortable with reading code and recognizing when lists are in play.

Ways to increase our skill include:
- Recognizing lists while reading code
- Recognizing lists while reading problems

## Learning Goals



## Recognizing Lists When Reading Python Code

We want to be so familiar with lists, that even when we read unfamiliar Python code, we can make strong guesses for when we come across a list.

To get to that familiarity, in this lesson, we will...

1. Read Python code
2. Write our own observations for how to recognize lists
3. Make conclusions about recognizing data and lists in Python

### Reading Code

Read this code below line-by-line and take notes about what's happening.

```python
def find_differences(sequence_1, sequence_2):
    differences = []
    if (len(sequence_1) != len(sequence_2)):
      print("These sequences aren't the same length! Let's stop comparing them!")
    elif (sequence_1[0] != sequence_2[0]):
        differences.append(sequence_1[0])
        differences.append(sequence_2[0])
    return differences

simons_dna = ['G', 'A', 'G', 'C', 'C', 'T']
beccas_dna = ['C', 'A', 'T', 'C', 'G', 'T']
find_differences(simons_dna, beccas_dna)
```

### Make Your Own Conclusions About Lists in Python Code

Share your notes about what you observed in the above code. **What pieces of syntax** directly helped you make those conclusions?


### Our Conclusions About Lists in Code

| Observation | When it's related to lists | Other notes
| --- | --- | ---
| Square brackets `[]` | Square brackets are a big indicator of lists. We use square brackets to **create list literals.** We use square brackets with an integer inside next to a list to _index_ into a list. `[]` is a list literal that is an empty list. | There are a few other pieces of Python syntax that use square brackets, so be careful to pay attention to context
| Plural variable name | Because lists contain **multiple elements,** we usually assign lists to variables with plural variable names. | This isn't a Python syntax rule, so it isn't enforced. This entirely depends on the context of the program.
| Using the word "append" | "Append" means adding something to the end of something. This word gets used commonly with lists. Lists specifically have a method named `append`, which adds an element to the end of the list. | Not many other things in Python use the word "append," although it's not a reserved word.
| Using the word "length" | A frequently used property for lists is its length. An empty list has a length of zero. We can use the `len` function and pass in a list to get its length. | Many different data types in Python have a "length" property, such as Strings!

Feel free to bring in any other conclusions missed in the above table!

## Recognizing Lists When Reading Problem Statements

We want to be so familiar with lists, that even when we read an unfamiliar programming problem, we can make strong guesses about when to use a list.

To get to that familiarity, in this lesson, we will...

1. Read an example problem statement
2. Write our own observations for how to recognize lists
3. Make conclusions about recognizing data and lists in problem-solving

### An Example Problem Statement

Compare these two sequences of DNA, which contain many pieces of DNA. They are similar, but not the same, based on the order and value of each piece. These two sequences are the same length.

| No. | Sequence |
| --- | --- |
| 1 | GAGCCTACTAACGGGAT
| 2 | CATCGTAATGACGGCCT

We can visualize the differences between the two sequences like so:

```bash
GAGCCTACTAACGGGAT
CATCGTAATGACGGCCT
^ ^ ^  ^ ^    ^^
```

Create a function. In this function:
- Make an array that contains will contain all of the differences between the two sequences.
- Find the differences between the two sequences.
    - Add each difference to the array of differences.

### Make Your Own Conclusions About Lists in Python Code

Share your notes about what you observed in the above problem statement. **What pieces of the problem statement** directly helped you make those conclusions?



### Our Conclusions About Lists in Problem Statements

| Observation | When it's related to lists | Examples
| --- | --- | ---
| Using the word "list" or "array" | Literally using the word "list" is a good indicator that a list could be involved
| Mentions of multiple "things" that are similar | A list usually groups similar things. Except for order (or depending on context), lists don't really have a way to represent one element being "more special" than another. Lists are great for lists of things of equal importance. | A list of groceries with no specific order, a list of letters in the alphabet, a list of books that are unavailable at the library
| Mentions of an order, sequence, or sorting to multiple things | A list keeps its elements in an order, so any mention of "order," "sequence," or "sorting." being important might be a sign of a list. | A priority list of groceries, where the highest priority is first. The alphabet song, in order. A list of unavailable books sorted by their due date.
| Mentions getting, using, comparing "one" element out of "many" | A problem that focuses comparing "one" (or a few) item to many others is a problem that lists can solve well. | Finding the highest priority grocery item. Counting how many letters in the alphabet are vowels. Finding all books with a due date of Sunday.
| Mentions referencing an element by index | A problem that mentions an element by its position (index) is a clue that a list is a good idea. | "The second item to buy is always coffee." "The alphabet should be replaced with `*` every fifth letter." "The `checkin` function should always grab the first book"
| Mentions adding or removing an element to a list | Lists are really great at growing and shrinking. | "The user should be able to add or remove any number of shopping items" "Remove any letter that isn't uppercase." "Add a book every time someone checks out a book."
| Mentions the length of a list | Lists can easily calculate its own length, and clues around constraints or freedoms around a list's length is a clue to use a list. | "The grocery list should never be over 15 items." "An alphabet can have an infinite number of characters," "Check the number of books every time we check out a book."

## Summary

We should continue to use lists to represent lists of ordered data.

When we read code, we can recognize list syntax in order to use lists more effectively. Pieces of code like square brackets `[]` are indicators of using lists.

When we read a problem statement, we can recognize key words in a problem to give us hints to use lists. Key words like order, index, elements, append, etc. can be clues to use lists to solve the problem.


## Check for Understanding

Write down an explanation about what "lists" (the data type in Python) are, as if explaining to a ten year old.



Describe some ways you can recognize that some code is using a list, based off of the syntax.



```python
materials = ["Wood", "Paper", "Cardboard"]
```

What is the data type of `materials`?

* String
* None
* Boolean
* List


Consider the list `["Wood", "Paper", "Cardboard"]`. Which of these is the most readable variable name?

* `material`
* `materials`
* `list`
* `l`





Which of these is the best representation of a grocery list in Python?

* `"Spinach, Broccoli, Eggplant, Potatoes"`
* `[Spinach, Broccoli, Eggplant, Potatoes]`
* `["Spinach", "Broccoli", "Eggplant", "Potatoes"]`
* `[["Spinach"], ["Broccoli"], ["Eggplant"], ["Potatoes"]]`


Describe some ways you can recognize that a problem's solution might use a list.



| Date (YYYY-MM-DD format) | Number of Crows Spotted in the Parking Lot |
| --- | --- |
| 2020-09-01 | 3
| 2020-09-02 | 5
| 2020-09-03 | 5
| 2020-09-04 | 6
| 2020-09-05 | 2
| 2020-09-06 | 2
| 2020-09-07 | 1
| 2020-09-08 | 0

Imagine this data is from an organization called "The Fellowship of Simon's Neighbors" that collects data on Simon's neighbors. Look through the data and make a prediction about what this data means and represents, and how you would explain it to a 10 year old.

Type the most important data out as one list, and store it in a variable. Choose your variable name wisely.


Create a variable named `hobbies` and assign it to a list that contains your own hobbies. Run this code to make sure you don't have any syntax errors or runtime errors.

```python

# Make a variable named hobbies in the line above this comment

print(f"My hobbies include {hobbies}")
```

Create a variable named `groceries` and assign it to a list that contains your own grocery list. Run this code to make sure you don't have any syntax errors or runtime errors.

```python

# Make a variable named groceries in the line above this comment

print(f"My grocery list includes {groceries}")
```

Here is a function named `add_grocery(grocery_list, new_item)`. Inside of the function body `add_grocery`, add code that will append the `new_item` to `grocery_list`.

```python
def add_grocery(grocery_list, new_item):
    pass
    # Replace pass with a new function body
    # that appends new_item to grocery_list

groceries = ["Spinach", "Broccoli", "Eggplants", "Potatoes"]
add_grocery(groceries, "Carrots")
```

Here is a function named `steal_top_food(my_groceries, their_groceries)`. This function takes in two grocery lists, `my_groceries` and `their_groceries`.This function should:

1. Read the first element from the list `their_groceries`, and store it into a local variable.
2. Replace (re-assign) the first element in `my_groceries` with the stored value (the local variable) from step 1.
3. Return the list `my_groceries`

Implement the function `steal_top_food`

```python
def steal_top_food(my_groceries, their_groceries):
    pass
    # Replace pass with a new function body
    # that fulfills the requirements

simons_groceries = ["Spinach", "Broccoli", "Eggplants", "Potatoes"]
devins_groceries = ["Avocados", "Oat Milk", "Mangoes"]
steal_top_food(simons_groceries, devins_groceries)
```