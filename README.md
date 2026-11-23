Python CI Integration Project
Project Overview
This project was developed as part of the YuvaIntern Junior Python Developer Internship - Week 6 Task: Integrating Continuous Integration (CI) in Python Projects.

The project implements a simple Grade Calculator application in Python and demonstrates the integration of a Continuous Integration (CI) pipeline using GitHub Actions. The CI pipeline automatically checks code quality and runs automated tests whenever code is pushed to the repository.

Objective
The objective of this project is to:

Develop a Python application with clear functionality.
Create automated tests using Pytest.
Implement code quality checks using Flake8.
Configure a Continuous Integration pipeline using GitHub Actions.
Automate testing and validation for every code change.
Project Features
Calculate grades based on student marks.
Input validation for invalid marks.
Automated unit testing.
Static code analysis using Flake8.
Automated CI workflow using GitHub Actions.
Technologies Used
Python 3.10
Pytest
Flake8
GitHub Actions
Git
GitHub
Project Structure
yuvaintern-week6-ci/
│
├── grade_calculator.py
├── test_grade_calculator.py
├── requirements.txt
├── README.md
└── .github/
    └── workflows/
        └── ci.yml
Application Logic
The Grade Calculator assigns grades according to the following criteria:

Marks Range	Grade
90 - 100	A
75 - 89	B
60 - 74	C
40 - 59	D
Below 40	Fail
The application also raises an error if marks are less than 0 or greater than 100.

Installation
Clone the repository:

git clone <repository-url>
Navigate to the project folder:

cd yuvaintern-week6-ci
Install dependencies:

pip install -r requirements.txt
Running the Application
Open Python shell:

from grade_calculator import calculate_grade

print(calculate_grade(95))
Expected Output:

A
Running Automated Tests
Execute:

python -m pytest
Expected Result:

6 passed
Running Code Quality Checks
Execute:

python -m flake8 .
If there are no issues, Flake8 will return without displaying any errors.

Continuous Integration Setup
The project uses GitHub Actions to automate the development workflow.

The CI pipeline performs the following tasks:

Checks out the repository code.
Sets up Python 3.10.
Installs project dependencies.
Runs Flake8 linting checks.
Runs Pytest automated tests.
Reports workflow status.
The workflow is automatically triggered when:

Code is pushed to the main branch.
A pull request is created for the main branch.
Test Cases
Test Grade A
Input:

calculate_grade(95)
Expected Output:

A
Test Grade B
Input:

calculate_grade(80)
Expected Output:

B
Test Grade C
Input:

calculate_grade(65)
Expected Output:

C
Test Grade D
Input:

calculate_grade(45)
Expected Output:

D
Test Fail Grade
Input:

calculate_grade(20)
Expected Output:

Fail
Test Invalid Marks
Input:

calculate_grade(120)
Expected Output:

ValueError
Benefits of Continuous Integration
Early detection of bugs.
Improved code quality.
Automated verification of code changes.
Consistent development workflow.
Reduced chances of introducing errors into the project.
Challenges Faced
During development, several challenges were encountered:

Configuring the project structure correctly.
Resolving Flake8 formatting errors.
Setting up Pytest automation.
Understanding GitHub Actions workflow configuration.
Ensuring all tests passed before deployment.
These challenges were resolved through debugging, validation, and careful workflow configuration.

Future Improvements
Potential enhancements include:

Code coverage integration.
Multiple Python version testing.
Continuous Deployment (CD) setup.
Security scanning automation.
Docker-based deployment pipeline.
Conclusion
This project successfully demonstrates the implementation of Continuous Integration in a Python project using GitHub Actions. Automated testing and linting were integrated into the workflow to ensure code quality and reliability. The project showcases how CI practices can improve software development efficiency and reduce the likelihood of defects reaching production.
