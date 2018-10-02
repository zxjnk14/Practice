# Use Case Model

**Author**: \<Team 79>

## 1 Use Case Diagram


## 2 Use Case Descriptions

*For each use case in the use case diagram, this section should contain a description, with the following elements:*


- *Requirements: High-level description of what the use case must allow the user to do.*
- *Pre-conditions: Conditions that must be true before the use case is run.*
- *Post-conditions Conditions that must be true once the use case is run.*
- *Scenarios: Sequence of events that characterize the use case. This part may include multiple scenarios, for normal, alternate, and exceptional event sequences. These scenarios may be expressed as a list of steps in natural language or as sequence diagrams.*

**1) Register**
- Requirements: The *Register* use case allows a student to register with the vocabulary quiz app. 
- Pre-conditions: The username provided by the new student must be unique, which means that the result from *Check Unique Username* must be true. The student must also provide a major, a seniority level and an email address to finish the registration.   
- Post-conditions: Once the register finishes, the student must be added to the list of existing students and is allowed to log in to the app. 
- Scenarios: 
    - The student opens the app and clicks on the 'Register' button.
    - The student types in a username.
    - The app will check if the username already exists. 
    - If the username is not unique, then the app will display an error message and ask the student to put in a new username again. 
    - If the username is unique, the app will allow the student to input a major, a seniority level and an email address. 
    - Once the registration complete, the student will be brought to the log in page. 

**2) Log In**
- Requirements: The *Log In* use case allows an existing student to log in to the quiz app. 
- Pre-conditions: The student can only log in to the app if the username he/she types in already exists in the database. 
- Post-conditions: After logging in, the student should be provided the options to a) add a quiz b) delete a quiz c) practice a quiz and d) view score statistics. 
- Scenarios:
    - The student opens the app and clicks on the 'Log In' button.
    - The student types in the username.
    - The app will check if the username already exists. 
    - If the username does not exist, an error message will be displayed and the student will be provided the option to log in or register. 
    - If the username exists the student will be provided the options to a) add a quiz b) delete a quiz c) practice a quiz and d) view score statistics. 

**3) Add Quiz**
- Requirements: The *Add Quiz* use case allows a student to add a quiz to the list of quizzes by providing a unique quiz name, a short description, a list of N words and their definitions and a list of 3*N incorrect definitions. 
- Pre-conditions: The student must be logged in to add a quiz in the app. The quiz name provided must be unique. 
- Post-conditions: The newly created quiz should be added to the list of quizzes in the app. The new quiz should be available for other students to practice. 
- Scenarios:
    - The student clicks on the 'Add Quiz' button. 
    - The student puts in a new quiz name. 
    - The app checks if the quiz name is unique. 
    - If the quiz name is not unique, the app will ask the student to put in a quiz name again
    - If the quiz name is unique, the app will ask the student put in the list of N words and their definitions and also a list of 3*N incorrect definitions. 

**4) Delete Quiz**
- Requirements: The *Delete Quiz* use case allows a student to delete a quiz created by him/herself from the list of quizzes.
- Pre-conditions: The student must be logged in to delete a quiz. The creator of the quiz must be the student him/herself. 
- Post-conditions: The quiz should be deleted from the list of quizzes in the app, together with the quiz statistics. 
- Scenarios:
    - The student clicks on the 'Delete Quiz' button. 
    - A list of quizzes avaialble will be displayed. 
    - The student selects one quiz from the list. 
    - The app will check the creator of the quiz. 
    - If the creator is not the student him/herself, the app will display an error message.
    - If the creator is the student him/herself, the quiz and its scores will be deleted. 

**5) Practice Quiz**
- Requirements: The *Practice Quiz* use case allows a student to practice a quiz not created by him/herself from the list of quizzes in the app. 
- Pre-conditions: The student must be logged in to practice a quiz. The quiz cannot be created by the student him/herself. 
- Post-conditions: If a student completes a quiz, the student username, score and datetime the quiz is completed should be recorded. 
- Scenarios:
    - The student clicks on 'Practice Quiz' button
    - A list of quizzes avaialble will be displayed. 
    - The student selects one quiz from the list. 
    - The app will check if the creator of the quiz is the student him/herself. 
    - If the creator is the student, the app will display an error message. 
    - If the creator is not the student him/herself, N questions will be generated based on the word-definition pairs and inccorect definitions available in the quiz. 
    - Each question will be displayed and the student will answer the question. 
    - The app will display the next question until all questions are used. 
    - When the student finishes all the questions in the app, the percentage of correct questions will be displayed. 
    - The student's username, score and datetime finishing the quiz will be saved.

**6) Answer Question**
- Requirements: The *Answer Question* use case allows a student to select a definition among the four definitions displayed for a question. 
- Pre-conditions: The student must be logged in and started a practice session to answer a question. 
- Post-conditions: The app should display "correct" or "incorrect" for this question based on the answer. The total number of correctly answered questions should be added by 1 if the answer is correct.
- Scenarios:
    - The app displays a question word and four definitions (one of the definitions is correct).
    - The student selects one of the definitions. 
    - The app should display "correct" if the answer is correct and "Incorrect" if the answer is not correct.
    - Total number of correct questions should be added by 1 if the answer is correct. 

**7) View List of Quiz Score Stats**
- Requirements: The *View List of Quiz Score Stats* use case allows a student to look at his/her quiz scores.  
- Pre-conditions: The student must be logged in to see quiz scores.
- Post-conditions: Quiz scores will be displayed.
- Scenarios
    - Student clicks on the 'View List of Quiz Score Stats' button.
    - All quizzes must be listed, ordered by the time they are last played by the student.
    - Student clicks on a certain quiz.
    - The app displays the student's first score and when it was achieved.
    - The app displays the student's highest score and when it was achieved. 
    - The app displays the names of the first three students who score 100% on the quiz, ordered alphabetically. 

