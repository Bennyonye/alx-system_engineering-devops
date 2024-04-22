# API

This project focused on gaining practical experience with APIs. I interacted with the [JSONPlaceholder REST API](https://jsonplaceholder.typicode.com/), gathering data and learning how to export it to either CSV or JSON formats.

## Tasks

* **0. Gather data from an API**
  * [0-gather_data_from_an_API.py](./0-gather_data_from_an_API.py): Python script that retrieves information about the to-do list progress of a specified employee ID.
  * Usage: `python3 0-gather_data_from_an_API.py <employee ID>`.
  * Output format: `Employee <employee name> is done with tasks(<# completed tasks>/<total # tasks>):`

* **1. Export to CSV**
  * [1-export_to_CSV.py](./1-export_to_CSV.py): Python script that exports to-do list information of a specified employee ID to CSV format.
  * Usage: `python3 1-export_to_CSV.py <employee ID>`
  * File name format: `<user id>.csv`.
  * CSV Format: `"<user id>","<username>","<task completed status>","<task title>"`.

* **2. Export to JSON**
  * [2-export_to_JSON.py](./2-export_to_JSON.py): Python script that exports to-do list information of a specified employee ID to JSON format.
  * Usage: `python3 2-export_to_JSON.py <employee ID>`
  * File name format: `<user id>.json`
  * JSON Format: `{ "<user id>": [ {"task": "<task title>", "completed": <task completed status>, "username": "<username>"}}, ... ]}`

* **3. Dictionary of list of dictionaries**
  * [3-dictionary_of_list_of_dictionaries.py](./3-dictionary_of_list_of_dictionaries.py): Python script that exports to-do list information for all employees to JSON format.
  * Usage: `python3 3-dictionary_of_list_of_dictionaries.py`
  * File name: `todo_all_employees.json`
  * JSON Format: `{ "<user id>": [ {"username": "<username>", "task": "<task title>", "completed": <task completed status>}, {"username": "<username>", "task": "<task title>", "completed": <task completed status>}, ... ], "<user id>": [ {"username": "<username>", "task": "<task title>", "completed": <task completed status>}, {"username": "<username>", "task": "<task title>", "completed": <task completed status>}, ... ]}`
