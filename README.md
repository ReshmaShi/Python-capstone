# CUSTOMER SUPPORT TICKET ANALYSER

## 1. Project Title

**Customer Support Ticket Analyser**

---

## 2. Project Overview

The **Customer Support Ticket Analyser** is a Python-based project used to store, clean, and analyse customer support tickets.

Customer support teams receive many tickets every day. Analysing these tickets helps identify common issues, understand ticket priorities, and find useful patterns in customer complaints and feedback.

This project uses Python concepts such as:

* Dictionary
* Lists
* Strings
* Sets
* `if / elif / else`
* `for` loop
* `while` loop
* Functions
* String methods
* List methods
* Basic data analysis

---

# 3. Problem Statement

Customer support teams handle numerous service tickets daily.

Manually analysing these tickets can be time-consuming. Therefore, a simple Python-based system is created to:

* Store customer ticket information
* Add new tickets
* Validate ticket priority
* Clean issue descriptions
* Search for important keywords
* Analyse ticket priorities
* Find the longest issue description
* Identify unique words used in customer issues

---

# 4. Objectives

The main objectives of this project are:

1. Store customer support ticket information.
2. Display ticket information in a readable format.
3. Allow users to add new tickets.
4. Automatically generate ticket numbers.
5. Validate ticket priorities.
6. Clean customer issue descriptions.
7. Count tickets containing specific keywords.
8. Analyse High, Medium, and Low priority tickets.
9. Find the ticket with the longest issue description.
10. Extract unique words from all ticket descriptions.

---

# 5. Tools and Technologies Used

### Programming Language

**Python**

### Python Concepts Used

* Dictionary
* List
* Set
* String
* Variables
* `input()`
* `print()`
* `len()`
* `append()`
* `replace()`
* `lower()`
* `strip()`
* `capitalize()`
* `split()`
* `join()`
* `sorted()`
* `if`
* `elif`
* `else`
* `for` loop
* `while` loop
* Functions
* `return`
* `break`

---

# 6. Dataset

The project initially contains 10 customer support tickets.

Each ticket contains four fields:

| Field             | Description              |
| ----------------- | ------------------------ |
| Ticket_No         | Unique ticket number     |
| Customer_Name     | Name of the customer     |
| Issue_Description | Customer's support issue |
| Priority          | Ticket priority          |

### Initial Ticket Count

**10 tickets**

The user can add additional tickets while running the program.

---

# 7. Project Workflow

The project follows these steps:

```text
Start
  ↓
Load Preloaded Tickets
  ↓
Display Initial Tickets
  ↓
Ask User to Add New Tickets
  ↓
Validate Priority
  ↓
Generate Ticket Number
  ↓
Add New Ticket
  ↓
Clean Issue Descriptions
  ↓
Keyword Analysis
  ↓
Priority Analysis
  ↓
Find Longest Issue
  ↓
Find Unique Words
  ↓
Display Final Results
  ↓
End
```

---

# 8. Step 1 — Preloaded Ticket Data

The project starts with a dictionary called `ticket_data`.

It contains four lists:

```python
ticket_data = {
    'Ticket_No': [...],
    'Customer_Name': [...],
    'Issue_Description': [...],
    'Priority': [...]
}
```

A dictionary is used because it allows related information to be stored using meaningful keys.

For example:

```python
ticket_data['Customer_Name']
```

accesses the customer names.

---

# 9. Step 2 — Adding New Tickets

The program asks the user:

```text
How many new tickets do you want to add?
```

For each new ticket, the user enters:

* Customer Name
* Issue Description
* Priority

The `input()` function is used to collect information from the user.

A `for` loop is used to repeat the process according to the number of tickets entered.

---

# 10. Priority Validation

The program accepts only three priority values:

* High
* Medium
* Low

A `while` loop is used to keep asking the user until a valid priority is entered.

The following methods are used:

### `strip()`

Removes unwanted spaces from the beginning and end of the input.

Example:

```text
" High "
```

becomes:

```text
"High"
```

### `capitalize()`

Converts the first letter to uppercase.

Example:

```text
"high"
```

becomes:

```text
"High"
```

This makes the input more consistent.

---

# 11. Automatic Ticket Number

The program automatically creates the next ticket number using:

```python
len(ticket_data['Ticket_No']) + 1
```

If there are currently 10 tickets:

```text
10 + 1 = 11
```

Therefore, the next ticket receives ticket number **11**.

This avoids manually entering ticket numbers.

---

# 12. Adding Data Using `append()`

The `append()` method is used to add new information to the end of a list.

Example:

```python
ticket_data['Customer_Name'].append(customer_name)
```

This adds the new customer's name to the customer list.

The same method is used for:

* Ticket number
* Customer name
* Issue description
* Priority

---

# 13. Step 3 — Text Cleaning

Customer descriptions may contain:

* Capital letters
* Extra spaces
* Punctuation
* Shorthand words

A function called `clean_text()` is created to clean the descriptions.

### Cleaning Operations

#### Convert to lowercase

```python
text.lower()
```

Example:

```text
"GREAT SUPPORT"
```

becomes:

```text
"great support"
```

---

#### Remove punctuation

The `replace()` method removes:

```text
.
,
!
?
```

Hyphens are replaced with spaces.

---

#### Replace shorthand

```python
text.replace("ok", "okay")
```

changes:

```text
ok
```

to:

```text
okay
```

---

#### Split the text

```python
text.split()
```

breaks a sentence into individual words.

Example:

```text
"good support service"
```

becomes:

```python
["good", "support", "service"]
```

---

#### Join the words

```python
" ".join(words)
```

joins the words together using one space.

This helps remove multiple spaces.

---

#### Remove outside spaces

```python
text.strip()
```

removes spaces from the beginning and end of the text.

---

# 14. Step 4 — Keyword Analysis

A function called:

```python
count_tickets_with_word(word)
```

is created.

Its purpose is to count how many ticket descriptions contain a particular word.

The project checks these keywords:

* `poor`
* `good`
* `slow`
* `excellent`

The description is split into individual words, and the program checks whether the searched word exists.

For example:

```python
count_tickets_with_word("poor")
```

returns
