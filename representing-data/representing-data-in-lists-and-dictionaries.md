# Representing Data in Lists and Dictionaries

## Learning Goals

- Practice representing ordered data as a list
- Practice representing related data as a list

## Introduction

As we see more and more problems in programming, we'll be faced with a lot of ambiguous direction. Exciting computer science problems will often have no obvious place to start. Should you make a function? How many variables? Do we need iteration?

As part of _breaking down a problem_, one step we should consider, take, and practice, is representing data we see as data structures. We want to practice the process of seeing given data described to us, and turning it into data structures like strings, lists, dictionaries, and more, in order to give us one possible starting point.

## Vocabulary and Synonyms

| Vocab | Definition | Synonyms | How to Use in a Sentence |
| ----- | ---------- | -------- | ------------------------ |


## Recognizing Lists When Reading Problem Statements

We want to be so familiar with lists, that even when we read an unfamiliar programming problem, we can make strong guesses about when to use a list.

To get to that familiarity, in this lesson, we will...

1. Consider the strengths of lists
1. Read an example problem statement
1. Write our own observations for how to recognize lists
1. Make conclusions about recognizing data and lists in problem-solving

### The Strengths of Lists

Considering the strengths of lists as a data structure will give us clues to when lists are very appropriate to consider.

Lists are great at...

| Strength                                  | Notes                                                                                                                               | How it's represented in code                                                                                         |
| ----------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| Lists contain 0+ elements                 | Lists contain multiple elements in a specific order. The elements don't need to be of the same type.                                | The syntax of a list literal is comma-separated elements. Lists could possibly be indicated by plural variable name. |
| Lists contain elements in an order        | Elements in a list are always in an order. This order could have zero significance, or it could have meaning based on how it's used | -                                                                                                                    |
| Lists have a property of length/size      | A frequently used property for lists is its length. An empty list has a length of zero.                                             | We can use the `len` function and pass in a list to get its length.                                                  |
| We can access elements in a list by index | If we know the index of an element in a list, we can get the element                                                                | We index with square brackets, `my_list[0]`                                                                          |
| We can add things to lists                | We can add elements to lists                                                                                                        | `my_list.append(new_element)` will add this element to the end of the list                                           |
| We can remove things to lists             | We can remove elements from lists                                                                                                   | `my_list.remove(value_to_remove)` will find the first instance of this value and remove it                           |

### An Example Problem Statement

Compare these two sequences of DNA, which contain many pieces of DNA. They are similar, but not the same, based on the order and value of each piece. These two sequences are the same length.

| No. | Sequence          |
| --- | ----------------- |
| 1   | GAGCCTACTAACGGGAT |
| 2   | CATCGTAATGACGGCCT |

We can visualize the differences between the two sequences like so:

```bash
GAGCCTACTAACGGGAT
CATCGTAATGACGGCCT
^ ^ ^  ^ ^    ^^
```

Create a function. In this function:

- Make a list that contains will contain all of the differences between the two sequences.
- Find the differences between the two sequences.
  - Add each difference to the list of differences.

### Make Your Own Conclusions About Lists in Python Code

Share your notes about what you observed in the above problem statement. **What pieces of the problem statement** directly helped you make those conclusions?

Learn Short Answer

### Our Conclusions About Lists in Problem Statements

| Observation                                                    | When it's related to lists                                                                                                                                                                                                           | Examples                                                                                                                                                               |
| -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Using the word "list" or "array"                               | Literally using the word "list" is a good indicator that a list could be involved                                                                                                                                                    |
| Mentions of multiple "things" that are similar                 | A list usually groups similar things. Except for order (or depending on context), lists don't really have a way to represent one element being "more special" than another. Lists are great for lists of things of equal importance. | A list of groceries with no specific order, a list of letters in the alphabet, a list of books that are unavailable at the library                                     |
| Mentions of an order, sequence, or sorting to multiple things  | A list keeps its elements in an order, so any mention of "order," "sequence," or "sorting." being important might be a sign of a list.                                                                                               | A priority list of groceries, where the highest priority is first. The alphabet song, in order. A list of unavailable books sorted by their due date.                  |
| Mentions getting, using, comparing "one" element out of "many" | A problem that focuses comparing "one" (or a few) item to many others is a problem that lists can solve well.                                                                                                                        | Finding the highest priority grocery item. Counting how many letters in the alphabet are vowels. Finding all books with a due date of Sunday.                          |
| Mentions referencing an element by position                    | A problem that mentions an element by its position (index) is a clue that a list is a good idea.                                                                                                                                     | "The second item to buy is always coffee." "The alphabet should be replaced with `*` every fifth letter." "The `checkin` function should always grab the first book"   |
| Mentions adding or removing an element to a list               | Lists are really great at growing and shrinking.                                                                                                                                                                                     | "The user should be able to add or remove any number of shopping items" "Remove any letter that isn't uppercase." "Add a book every time someone checks out a book."   |
| Mentions the length of a list                                  | Lists can easily calculate its own length, and clues around constraints or freedoms around a list's length is a clue to use a list.                                                                                                  | "The grocery list should never be over 15 items." "An alphabet can have an infinite number of characters," "Check the number of books every time we check out a book." |

## Summary

## Check for Understanding

```python
materials = ["Wood", "Paper", "Cardboard"]
```

What is the data type of `materials`?

- String
- None
- Boolean
- List

Consider the list `["Wood", "Paper", "Cardboard"]`. Which of these is the most readable variable name?

- `material`
- `materials`
- `list`
- `l`

Which of these is the best representation of a grocery list in Python?

- `"Spinach, Broccoli, Eggplant, Potatoes"`
- `[Spinach, Broccoli, Eggplant, Potatoes]`
- `["Spinach", "Broccoli", "Eggplant", "Potatoes"]`
- `[["Spinach"], ["Broccoli"], ["Eggplant"], ["Potatoes"]]`

Describe some ways you can recognize that a problem's solution might use a list.

| Date (YYYY-MM-DD format) | Number of Crows Spotted in the Parking Lot |
| ------------------------ | ------------------------------------------ |
| 2020-09-01               | 3                                          |
| 2020-09-02               | 5                                          |
| 2020-09-03               | 5                                          |
| 2020-09-04               | 6                                          |
| 2020-09-05               | 2                                          |
| 2020-09-06               | 2                                          |
| 2020-09-07               | 1                                          |
| 2020-09-08               | 0                                          |

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
