# Student Score Prediction
The objective of this project is to analyze how parental background, test preparation, and the ethnicity of a student impact the students' math scores.



## Technologies Used
</h3>
<br>
<p align="left">
        <img width="48" height="48" src="https://img.icons8.com/fluency/48/python.png" alt="python"/>
        <img width="48" height="48" src="https://img.icons8.com/fluency/48/jupyter.png" alt="jupyter"/>
        <img width="48" height="48" src="https://img.icons8.com/color/48/amazon-web-services.png" alt="amazon-web-services"/>
        <img width="48" height="48" src="https://img.icons8.com/color/48/artificial-intelligence.png" alt="artificial-intelligence"/>
        <img width="55" height="55" src="https://img.icons8.com/nolan/64/flask.png" alt="flask"/>
        <img width="48" height="48" src="https://img.icons8.com/color/48/git.png" alt="git"/>

</p>
</div>
<br>

`Python`  `Jupyter Notebook` `AWS Elastic Beanstalk`  `CI/CD Pipelines`  `Machine Learning Algorithms`  `Flask`  `Git`

## Dataset
There are 8 independent variables:

- `gender` : Sex of a student (Male/Female)
- `race/ethnicity` : Ethnicity of a student (Group A,B,C,D,E)
- `parental level of education` : parents' final education (bachelor's degree,some college,master's degree,associate's degree,high school)
- `lunch` : What type of lunch the student had before test (standard or free/reduced)
- `test preparation course` : Whether the student completed any preparation course before the test.
- `reading score` : Reading score obtained by the student.
- `writing score` : Writing score obtained by the student.

Target variable:

- `math score`: Math score of a student.

Dataset Source Link :
[https://www.kaggle.com/datasets/spscientist/students-performance-in-exams?resource=download](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams?resource=download)

## Application Demo
![Untitled_Project_V2](https://github.com/user-attachments/assets/958ce035-cf81-47a7-a3cf-8adf533585e3)

## Project Development Approach
1. Data Ingestion:

- Data was read from a CSV file.
- Data was split into training and testing sets.
- Training and testing sets were saved as separate CSV files.
- Data Transformation:

2. A ColumnTransformer Pipeline was created.
- For numeric variables:
- SimpleImputer with the median strategy was applied.
  
- For categorical variables:
- SimpleImputer with the most frequent strategy was applied.
- One-hot encoding was performed.

- The preprocessor was saved as a PKL file in the artifacts folder.

3. Model Training:
- Various models were trained and evaluated.
- Linear Regression was selected as the best-performing model.
- Hyperparameter tuning was performed.
- The final model was saved as a PKL file.

4. Prediction Pipeline:
- Input data was converted into a DataFrame.
- Necessary PKL files were loaded.
- Predictions were generated using the trained model.

5. Flask App Creation:

- A Flask app was developed with a user interface for predicting math scores.
- Users were able to input data and receive predictions.

6. Deployment:

- The application was deployed using AWS Elastic Beanstalk.
- CI/CD pipelines were implemented for automated updates and maintenance.
