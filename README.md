# Hogwarts Student Sorting System	

## Sorting Hat Script (`sorting_hat.py`)

The Sorting Hat script (`sorting_hat.py`) is designed to sort students into Hogwarts houses based on their characteristics and birthdates. It also generates a CSV report with student names, assigned houses, and corresponding grades.

## Usage

To use the Sorting Hat script, follow these steps:

##### 1-Ensure you have a valid CSV file containing student data. The CSV file should have columns named "characteristic" and "birthdate."

##### 2-Run the script by executing the following command:

	python sorting_hat.py input.csv output.csv
  
Replace `input.csv` with the path to your input CSV file and `output.csv` with the desired output file name	

##### 3-Review the output: The script will generate a new CSV file (`output.csv`) with the assigned houses and grades for each student.

## Input CSV Format

Ensure that your input CSV file follows this format:
	
   	name,characteristic,birthdate
	Harry Potter,courage,1980
	Hermione Granger,wisdom,1979
	Ron Weasley,loyalty,1980
	...





## CSV Report	 `&&`     Output CSV Format

The script generates a CSV report containing the following columns  `&&` The output CSV file will have the following columns:


`name:`Student's name	

`house:`Assigned Hogwarts house	

`grade:`Assigned grade based on birthdate


### Error Handling

The script includes error handling for invalid input arguments, missing files, and invalid birth years.

`Incorrect number of command-line arguments:` If there are too few or too many command-line arguments, the script will exit with an appropriate message.

`Invalid file format:` If the provided files are not CSV files, the script will exit with an error message.

`File not found:` If the input CSV file is not found, the script will exit with an appropriate error message.

`Invalid birth year:` If a birth year is not a valid integer, the script will print an error message and assign an "Invalid Grade."

`No matching house:` If the characteristic does not match any house, the script will assign "No House."


## Testing Script (test_sorting_hat.py)

The testing script (`test_sorting_hat.py`) includes test cases for the Sorting Hat script. It utilizes the `pytest` framework.

## Test Functions

### 1-test_check_correct_args

This test checks if the check_correct_args function raises a SystemExit exception.

## 2-test_select_house

This test checks the `select_house` function, which assigns a Hogwarts house based on certain traits:


#### .`assert select_house("courage") == "Gryffindor"`
#### .`assert select_house("dedication") == "Hufflepuff"`
#### .`assert select_house("wisdom") == "Ravenclaw"`
#### .`assert select_house("ambition") == "Slytherin"`


### 3. test_select_grade

This test checks the `select_grade` function, which assigns a grade based on a given birth year:


#### . `assert select_grade("2005") == "Grade 14"`
#### . `assert select_grade("2015") == "Grade 4"`

### How to Run Tests

To run the tests, ensure you have the `pytest` library installed. You can install it using:

	pip install pytest

After installation, run the tests with:

	pytest test_sorting_hat.py




### By : Atia Mohamed 
### [Github](https://github.com/Rodex0010) 


























