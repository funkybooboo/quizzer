# Quiz Application

A simple interactive quiz application written in Python. The application loads questions from a JSON file, presents them to the user, and tracks their score based on correct and incorrect answers.

## Features

- Load questions from a JSON file.
- Shuffle questions for randomness.
- Allow user to specify the number of questions.
- Track correct and incorrect answers.
- Option to retry questions.
- Clear console screen for better readability.

## Requirements

- Python 3.x
- `colorama` library for colored text output.

You can install the `colorama` library using pip:

```bash
pip install colorama
```

## JSON Format for Questions

The application expects a JSON file named `questions.json` in the same directory. The format should be as follows:

```json
{
    "question1": {
        "prompt": "Which of the following are programming languages?",
        "answer": ["Python", "Java"],
        "distractors": ["HTML", "CSS", "SQL"]
    },
    "question2": {
        "prompt": "Select all prime numbers from the list.",
        "answer": ["2", "3", "5", "7"],
        "distractors": ["4", "6", "8", "9"]
    },
    "question3": {
        "prompt": "Which of these are fruits?",
        "answer": ["Apple", "Banana", "Cherry"],
        "distractors": ["Carrot", "Lettuce", "Potato"]
    },
    "question4": {
        "prompt": "Which of the following are countries in Europe?",
        "answer": ["France", "Germany", "Italy"],
        "distractors": ["Brazil", "Canada", "Australia"]
    },
    "question5": {
        "prompt": "Select the colors in the rainbow.",
        "answer": ["Red", "Green", "Blue", "Yellow"],
        "distractors": ["Pink", "Brown", "Black"]
    }
}
```

### Explanation of JSON Structure

- Each question is represented as a dictionary.
- The `prompt` field contains the question text.
- The `answer` field is a list of correct answers.
- The `distractors` field is a list of incorrect options.

## How to Run

1. Ensure you have Python 3.x installed.
2. Install the required libraries.
3. Create a `questions.json` file with your quiz questions.
4. Run the application:

```bash
python quiz.py
```

## Usage

- When prompted, enter the number of questions you want to attempt or type "all" for all available questions.
- To exit the application, type "exit" at any input prompt.
- Follow the on-screen instructions to answer the questions.

## Code Structure

- `main()`: The main entry point of the application.
- `is_integer(s)`: Helper function to check if a string is an integer.
- `quiz(questions)`: Handles the quiz logic and user interactions.
- `question_prompt(prompt, options)`: Displays the question and options to the user.
- `load_questions()`: Loads questions from the `questions.json` file.
- `clear_screen()`: Clears the console screen based on the operating system.

## License

This project is open-source and free to use. Contributions are welcome!
