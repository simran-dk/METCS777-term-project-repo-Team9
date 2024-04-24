# LinkedIn: Navigating Career Success - CS777 Term Project - Team 9

## Getting Started
After cloning this repo, run the following commands from the root directory:

1. Set up a python virtual env by running: `python -m venv venv`
2. Activate the virtual venv: `source venv/bin/activate`
3. Install the required dependencies: `pip3 install -r requirements.txt`

## Our Data
We decided to scrape LinkedIn public profiles for our dataset. We have structured our dataset into the following JSON structure.

Using PySpark we were to read in the structured data, load into a dataframe and rdd and run analysis.

```python
root
 |-- activity: struct (nullable = true)
 |    |-- connections: string (nullable = true)
 |    |-- followers: string (nullable = true)
 |-- education: array (nullable = true)
 |    |-- element: struct (containsNull = true)
 |    |    |-- dates_attended: struct (nullable = true)
 |    |    |    |-- end: string (nullable = true)
 |    |    |    |-- start: string (nullable = true)
 |    |    |    |-- total_time: string (nullable = true)
 |    |    |-- degree: array (nullable = true)
 |    |    |    |-- element: array (containsNull = true)
 |    |    |    |    |-- element: string (containsNull = true)
 |    |    |-- school_name: string (nullable = true)
 |-- education_count: long (nullable = true)
 |-- experience_count: long (nullable = true)
 |-- experiences: array (nullable = true)
 |    |-- element: struct (containsNull = true)
 |    |    |-- company_name: string (nullable = true)
 |    |    |-- positions: array (nullable = true)
 |    |    |    |-- element: struct (containsNull = true)
 |    |    |    |    |-- description: string (nullable = true)
 |    |    |    |    |-- end: string (nullable = true)
 |    |    |    |    |-- job_title: string (nullable = true)
 |    |    |    |    |-- start: string (nullable = true)
 |    |    |    |    |-- total_duration: string (nullable = true)
 |-- id: string (nullable = true)
 |-- last_generated_at: string (nullable = true)
 |-- skills: array (nullable = true)
 |    |-- element: string (containsNull = true)
 |-- skills_count: long (nullable = true)
```