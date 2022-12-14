# File generator

The file generator tech test comes with a mock data CSV that represents one of the many types of data that we have to deal with.

The challenge is to consume and transform the CSV file in to a nested JSON file which will form a tree structure.

## Getting Started

Use this repository as a starting point with the CSV file readily available in the root.

### Prerequisites

Use any IDE or resources that you would like. You can attempt this using any technologies you like, make sure you justify your choices.

## The desired form

From the CSV, you will see that the data follows a parent child structure. The first entry is always at the top of the tree, with the following entries being children of the previous column. The example below shows the structure that we would like to see.

```
{
  "label": "Meat & Fish",
  "id": "179549",
  "link": "https://groceries.retailer.com/browse/179549",
  "children": [
    {
      "label": "3 For £9.00 Meat & Poultry",
      "id": "179545",
      "link": "https://groceries.retailer.com/browse/179549/179545",
      "children": []
    },
    {
      "label": "Fish",
      "id": "176741",
      "link": "https://groceries.retailer.com/browse/179549/176741",
      "children": [
        {
          "label": "Fish Counter",
          "id": "176780",
          "link": "https://groceries.retailer.com/browse/179549/176741/176780",
          "children": [
            {
              "label": "Salmon",
              "id": "176979",
              "link": "https://groceries.retailer.com/browse/179549/176741/176780/176979",
              "children": []
            }
          ]
        }
      ]
    }
  ]
}
```
## Tasks
The task is to convert the provided CSV into JSON (see the example for the structure desired).

Remember that we would prefer the beginner task done well rather than all three done poorly. These menus can vary drastically in size and nesting, therefore you should remain aware of that when writing your solution and think about more columns and rows being in other CSV files that may be processed by your solution.

Please separate your tasks into feature branches using git-flow. `feature/beginner feature/intermediate feature/advanced`

### Beginner
Create a simple application that can run locally on a unix environment that has uses some sort of package management tool for your chosen language. There should be a few unit tests testing the main logic of your program.

### Intermediate
Your working solution should be dockerised and be able to be executed as an task on cloud platform. Also contain unit and integration tests.

### Advanced
Given you have completed the first two tasks. A CI/CD pipeline should be created to allow automatic deployment and running of tests. End to end tests should be created to test your solution on your chosen cloud platform. You should aim to have a solution that can be used by a non technical user and supply some interface for them to upload a csv file. 


## Deliverables

Replace the contents of this README.md with:

A covering note explaining the technology choices you have made.

1. Any instructions required to run your solution and tests in a Linux environment.
2. Email as an attachment or a link the git bundled repository showing your commit history with all your commits on the master branch:

<<<<<< feature/beginner
```
    git bundle create <anything>.bundle --all
```
=======

```
    git bundle create <anything>.bundle --all
```


<<<<< main
"""Feature/Begginer Task:-
GitHub Link:- https://github.com/Chandra314S/cognizant_tech_test_beginner.git

Step1:-
-- Check conda is installed in your PATH, cmd:- "conda -V".
-- Check conda is up to date, cmd:- "conda update conda".
-- Create a virtual environment, cmd:- "conda create -n yourenvname python=3.10".
-- Activate your virtual environment, cmd:- "conda activate yourenvname".
-- Install flask Web framework "pip install flask".
-- Run this command in command prompt "python app.py" to make the application live.
-- Open the browser and browse to the URL shown after the flask application is live Link:- "http://192.168.1.86:5000".
-- Drag & Drop or browse the .csv file.
-- Click Upload,
application internally performs the parsing and appropriate routing and will downloads the .json parsed file in to the local system of the user.

Step2:- (Performing UnitTesting)

-- Two test cases have been included in the Unittests.py file.
-- Run the unit tests by executing "python Unittests.py", It will show the status of the tests.

Technologies Used:- 
Python(Flask web framework), Bootstrap,CSS,html. """
