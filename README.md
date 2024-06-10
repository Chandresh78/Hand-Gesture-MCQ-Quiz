# Hand Gesture MCQ Quiz

This project is a Multiple-Choice Question (MCQ) quiz application that uses hand gestures to select answers. The project leverages OpenCV for video capture and image processing, and the `cvzone` library for hand detection and drawing utilities.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [CSV File Format](#csv-file-format)
- [How It Works](#how-it-works)
- [Dependencies](#dependencies)
- [Acknowledgements](#acknowledgements)

## Installation

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/your-repo/hand-gesture-mcq-quiz.git
   ```

2. Install the required dependencies:

   ```bash
   pip install opencv-python
   pip install cvzone
   ```

3. Ensure you have a webcam connected to your machine.

## Usage

1. Prepare your CSV file with the MCQs. Follow the format specified in the [CSV File Format](#csv-file-format) section.
2. Update the path to your CSV file in the script:

   ```python
   pathCSV = "path/to/your/Mcqs.csv"
   ```

3. Run the script:

   ```bash
   python hand_gesture_mcq_quiz.py
   ```

4. Use your hand to interact with the quiz. Pinch with your thumb and index finger to select an answer.

5. Press 'q' to quit the quiz at any time.

## CSV File Format

Your CSV file should contain the MCQs in the following format:

```
Question,Choice1,Choice2,Choice3,Choice4,Answer
How many corners does a triangle have?, Two, Three, Four, Five,2
What is the variable type of a? a = 'yes', Integer, Float, String, Character, 3
What is 2+2?,3,4,5,6,2
```

- **Question**: The question to be displayed.
- **Choice1 to Choice4**: The four possible answers.
- **Answer**: The index of the correct answer (1-based index).

## How It Works

1. The application captures video from the default camera using OpenCV.
2. Hand gestures are detected using the `cvzone.HandTrackingModule`.
3. The current question and choices are displayed on the screen.
4. The user can select an answer by pinching with their thumb and index finger.
5. The quiz progresses to the next question after a short delay.
6. At the end of the quiz, the user's score is displayed.

## Dependencies

- OpenCV
- cvzone
- Python 3.x

## Acknowledgements

- [OpenCV](https://opencv.org/)
- [cvzone](https://github.com/cvzone/cvzone)
