# python-homework
#### Assignment to show learning of topics over the last several weeks in Rice University FinTech Bootcamp!

---

## Table of contents
* [General info](#general-info)
* [Screenshots](#screenshots)
* [Technologies](#technologies)
* [Installation Guide](#installation-guide)
* [Code Examples](#code-examples)
* [Usage](#usage)
* [Status](#status)
* [Contributors](#contributors)

---

## General Information
#### The following repository contains two activities.  The first activity includes resources and files in the PyBank directory to pull in data from a .csv file, analyse the data to find various metrics, and produce a summary to the screen along with a summary.txt file.  The second optional activity relates to the resources and files in the PyRamen directory to pull in data from a .csv file, analyse the data to find various metrics, and produce a report to a .txt file.

---

## Screenshots
* PyBank information shown below
![PyBank Initial Run](./Images/PyBank_Initial_Run.png)

Output Summary

![PyBank Run Summary](./Images/PyBank_Output_Summary.png)

---

## Technologies
    * Python - Version 3.8.5
    * VS Code - Version 1.49.1
    * Jupyter Notebook - Version 6.1.1
    * Windows 10
    * Library - pathlib
    * Library - myfunctions

---

## Installation Guide
1. Download entire python-homework repository
2. Open Git Terminal
    
    ![Open Git Terminal](./Images/PyBank_Open_Git_Terminal.png)
    
3. Navigate into repository file path where the repository downloaded.

    ![Navigate to Repository](./Images/PyBank_Navigate_Into_Repo.png)

4. The files should be visible and ready to run.  *See [Usage](#usage) section below for instructions on how to run the program.

* Optional: PyRamen data files are included in the same repository for easy access.
    
---

## Code Examples
- PyBank: A summary output function to print a specific formatted summary to the screen and output a summary.txt file.

``` python
def summary_output(number_of_months_in_budget, net_total_amount_of_profits_and_losses, average_of_profit_and_losses, 
greatest_increase_date, greatest_increase_number, greatest_decrease_date, greatest_decrease_number):
    """Accepts metric variables and prints a standard output to the screen along with a summary.txt file to the 
        same location as the myfunctions libary.
    
    Args:
        number_of_months_in_budget (int): The number of months in the budget
        net_total_amount_of_profits_and_losses (int): The total amount of combined profits and losses.
        average_of_profit_and_losses (int): The average value of profits and losses.
        greatest_increase_date (str): The greatest increase date
        greatest_increase_number (int): The greatest increase number
        greatest_decrease_date (str): The greatest loss date
        greatest_decrease_number (int): The greatest loss number

    Output:
        Outputs summary message to screen and ./Output/summary.txt
    """

    # Capture file path to be written
    output_path = Path("./summary.txt")

    # Open output path 
    filewriter = open(output_path, 'w+')

    # Formatting individual rows for summary output and concatinates each string
    summary_message = "" 
    summary_message += "Financial Analysis\n"
    summary_message += "----------------------------\n"
    summary_message += f"Total Months: {number_of_months_in_budget}\n"
    summary_message += f"Total: ${net_total_amount_of_profits_and_losses}\n"
    summary_message += f"Average Change: ${average_of_profit_and_losses}\n"
    summary_message += f"Greatest Increase in Profits: {greatest_increase_date} (${greatest_increase_number})\n"
    summary_message += f"Greatest Decrease in Profits: {greatest_decrease_date} (${greatest_decrease_number})\n"
    
    # Outputs summary message to screen
    print(summary_message)

    # Writes summary message to output path
    filewriter.write(summary_message)

    # Closes file
    filewriter.close()
```

- A function to calculate the sum of key values in a list of dictionaries and return the sum.

``` python
def calculate_sum(list_of_dictionaries, key_name):
    """Accepts a list of dictionaries and loops through the list adding each key value.
    
    Args:
        list_of_dictionaries (list): A list of dictionaries
        key_name (str): The name of the key in the dictionaries to sum

    Returns:
        The sum of all the specified key values in the list.
    """

    # Initialize variables
    sum = 0

    # Loop through list
    for a_dictionary in list_of_dictionaries:

        # Add key values to sum variable
        sum += a_dictionary[key_name]
        
    return sum
```

---

## Usage
1. To run the process, navigate to the directory where main.ipynb is located using Git Terminal within the PyBank directory.  The PyRamen process can be run using the same steps below by navigating to the PyRamen directory.  PyRamen will only produce a summary.txt file.

    ![Navigate to Repository for main.py](./Images/PyBank_Path_Where_Main.ipynb_Is_Located.png)

2. Execute the command 'code .' in the terminal to open VS Code.

    ![Navigate to Repository for main.py](./Images/PyBank_Open_VS_Code.png)

3. VS Code opens.  Select the main.ipynb file in the PyBank directory.

    ![Open VS Code and select main.ipynb](./Images/PyBank_OpenVS_Select_Main.ipynb.png)

4. Click the Run All Cells button, double arrows, to run all cells in the Jupyter Notebook file.

    ![Run All Cells](./Images/PyBank_Click_Run_All_Cells.png)

5. All cells in the notbook run and a summary displays at the bottom of the screen along with a summary.txt file created in the root of the PyBank directory.

    ![Summary Output](./Images/PyBank_Output_Summary.png)
    
    ![Summary.txt in root directory](./Images/PyBank_Summary.txt_File.png)

---

## Status
Project is:
    - PyBank: _complete_
    - PyMenu: _complete_

---

## Contributors

* Jonathan Owens
* LinkedIn: www.linkedin.com/in/jonowens

