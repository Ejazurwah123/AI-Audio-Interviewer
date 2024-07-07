# CV-Based Interview Assistant

This is a Python-based application that helps conduct an interview process based on the information extracted from a candidate's CV (Curriculum Vitae). The application uses natural language processing techniques to analyze the CV, extract relevant information, generate interview questions, and evaluate the candidate's responses.

## Features

1. **CV Parsing**: The application reads a CV file and extracts the following information:
   - Sentences from the CV text
   - Named entities and their types
   - Top skills mentioned in the CV
   - A summary of the CV content

2. **Question Generation**: Based on the extracted information, the application generates the following types of interview questions:
   - Entity-based questions: Questions related to the candidate's experience with specific entities (e.g., projects, companies, etc.) mentioned in the CV.
   - Skill-based questions: Questions about the candidate's utilization of their top skills in previous roles.
   - Summarization-based questions: Questions that ask the candidate to elaborate on specific aspects of the CV summary.

3. **Follow-up Questions**: The application also generates a set of follow-up questions to further explore the candidate's responses.

4. **Interview Simulation**: The application conducts a simulated interview with the candidate, where it:
   - Reads the interview questions aloud using text-to-speech (TTS) functionality.
   - Prompts the candidate to answer the questions.
   - Analyzes the candidate's responses for factual information, general knowledge, and harsh or non-serious responses.
   - Scores the candidate's performance based on the analysis.
   - Provides a final result (selected or not selected) based on the candidate's overall score.

5. **Text-to-Speech (TTS) Integration**: The application uses the `gtts` (Google Text-to-Speech) library to generate and play the audio for the interview questions and responses.

## Requirements

- Python 3.6 or later
- The following Python libraries:
  - `spacy` (for natural language processing)
  - `collections` (for Counter)
  - `re` (for regular expressions)
  - `random` (for generating random data)
  - `wikipedia` (for retrieving information)
  - `textblob` (for text analysis)
  - `gtts` (for text-to-speech functionality)
  - `os` (for interacting with the operating system)

You can install the required libraries using pip:

```
pip install spacy textblob gtts
python -m spacy download en_core_web_sm
```

## Usage

1. Prepare a CV file (e.g., `cv.txt`) containing the candidate's resume information.
2. Run the `cv_interview_assistant.py` script:

```
python cv_interview_assistant.py
```

The application will:
- Extract information from the CV file.
- Generate interview questions and follow-up questions.
- Conduct a simulated interview with the candidate.
- Provide the final interview result (selected or not selected) based on the candidate's performance.

The audio for the interview questions and responses will be played using the system's default audio player.

## Customization

You can customize the application by modifying the following aspects:

1. **Answer Analysis**: The `analyze_answers` function in the `cv_interview_assistant.py` file is left empty, as you'll need to implement the logic to analyze the candidate's answers for factual information, general knowledge, and harsh or non-serious responses. You can use the `TextBlob` library or other natural language processing techniques to implement this functionality.

2. **Scoring and Selection Criteria**: You can adjust the scoring logic and the criteria for selecting or not selecting the candidate based on their performance.

3. **Question Generation**: You can modify the `generate_questions` function to customize the types of questions generated or add additional question categories.

4. **Text-to-Speech (TTS) Configuration**: If you prefer to use a different TTS library or engine, you can replace the `gtts` implementation with your preferred solution.

5. **CV File Format**: The application currently assumes the CV is provided as a plain text file (`cv.txt`). You can modify the `extract_sentences` function to handle different file formats, such as PDF or Word documents.

## Limitations

- The application relies on the accuracy of the natural language processing models and the quality of the CV data. Poorly formatted or incomplete CVs may affect the performance of the application.
- The answer analysis functionality is not implemented in the provided code, and you'll need to develop your own logic to evaluate the candidate's responses.
- The text-to-speech functionality may not work on all platforms or systems, depending on the availability of the required dependencies.

## Contributions

Contributions to this project are welcome. If you have any suggestions, bug reports, or improvements, please feel free to open an issue or submit a pull request on the project's GitHub repository.

## License

This project is licensed under the [MIT License](LICENSE).
