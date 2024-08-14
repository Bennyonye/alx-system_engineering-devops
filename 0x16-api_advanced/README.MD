# Advanced API Querying

This project extends my experience with API interactions, focusing on the Reddit API to perform various data retrieval tasks.

## Tests :heavy_check_mark:

* [Tests Folder](./tests): Contains test files for all tasks, as provided by ALX.

## Function Prototypes :floppy_disk:

The following prototypes were implemented in this project:

| File           | Prototype                                       |
| -------------- | ----------------------------------------------- |
| `0-subs.py`    | `def number_of_subscribers(subreddit):`         |
| `1-top_ten.py` | `def top_ten(subreddit):`                       |
| `2-recurse.py` | `def recurse(subreddit, hot_list=[]):`          |
| `100-count.py` | `def count_words(subreddit, word_list):`        |

## Project Tasks :page_with_curl:

* **1. Subscriber Count**
  * [0-subs.py](./0-subs.py): Implements a Python function that retrieves the total number of subscribers for a specified subreddit.
  * Returns `0` for invalid subreddits.

* **2. Top Ten Posts**
  * [1-top_ten.py](./1-top_ten.py): Python function that prints the top ten hottest posts for a specified subreddit.
  * Returns `None` for invalid subreddits.

* **3. Recursion for All Titles**
  * [2-recurse.py](./2-recurse.py): Python function that recursively retrieves all titles for hot articles in a specified subreddit.
  * Returns `None` if no results are found.

* **4. Keyword Counting**
  * [100-count.py](./100-count.py): Python function that recursively counts and prints a sorted list of specified keywords from the titles of hot articles in a subreddit.
  * The function is case-insensitive, sorting results first by frequency and then alphabetically.
  * Skips words with no matches and treats repeated words as separate instances.

---