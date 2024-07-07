# AI Interviewer
This project demonstrates how to use natural language processing (NLP) techniques to analyze the content of a CV and generate relevant questions for the candidate.

## Features

1. **Entity Extraction**: Identify key entities in the CV, such as people, organizations, locations, and job titles, using named entity recognition (NER).
2. **Skill Identification**: Analyze the CV text to extract the candidate's skills, both technical and soft skills.
3. **Summarization**: Generate a summary of the most important information in the CV.
4. **Question Generation**: Based on the insights gained from the above techniques, generate entity-based, skill-based, and summarization-based questions, as well as follow-up questions.
5. **Answer Evaluation**: Analyze the candidate's answers to determine if they are factual with respect to the CV content and whether they are general knowledge.

## Usage

1. Ensure you have the required dependencies installed:
   - `spacy`
   - `wikipedia`

2. Replace `"path/to/your/cv.txt"` in the code with the actual path to your CV file.

3. Run the script:

   ```
   python cv_question_generator.py
   ```

4. The script will output the generated questions and prompt you to enter answers for each one.

5. The script will then evaluate the answers and provide feedback on their factuality and whether they are general knowledge.

## Example Output

```
Questions:
Can you tell me more about your experience with Google?
Your answer: I worked at Google for 3 years as a software engineer. I was part of the team that developed the company's search algorithm.
Is the answer factual with respect to the CV? True
Is the answer general knowledge? True

How have you applied your Python expertise in your previous roles?
Your answer: I have used Python extensively in my previous roles to develop data analysis tools and automate various tasks. Python's versatility and large ecosystem of libraries have been invaluable in improving productivity and efficiency.
Is the answer factual with respect to the CV? True
Is the answer general knowledge? False

I noticed the summary mentioned machine learning. Can you elaborate on that and your specific contributions?
Your answer: In my previous role, I was part of the team that developed a machine learning-based recommendation system. I was responsible for feature engineering, model training, and deployment of the system, which helped the company improve user engagement and retention.
Is the answer factual with respect to the CV? True
Is the answer general knowledge? False

Follow-up Questions:
What was your role in the Google?
Your answer: As a software engineer at Google, I was responsible for developing and improving the company's search algorithm. I worked closely with the data science team to analyze user behavior and incorporate new signals into the algorithm.
Is the answer factual with respect to the CV? True
Is the answer general knowledge? True

What was your role in the machine learning?
Your answer: In my machine learning project, I was the lead engineer responsible for the end-to-end development of the recommendation system. This included data preprocessing, feature engineering, model training, and deployment of the system to production.
Is the answer factual with respect to the CV? True
Is the answer general knowledge? False
```

## Future Improvements

- Incorporate sentiment analysis to better understand the candidate's personality and work style.
- Develop more advanced summarization techniques to extract the most relevant information from the CV.
- Implement context-aware question generation to tailor the questions to the specific job requirements and company culture.
- Enhance the answer evaluation process to provide more detailed feedback and suggestions for the candidate.

## Contributing

If you have any suggestions or improvements, feel free to open an issue or submit a pull request.
