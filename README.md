# AI-Attendance-System-with-Facial-_Recognition-and-Emotion_Analysis
This project implements an AI-powered attendance system using facial recognition and emotion analysis. Built with DeepFace and OpenCV within a Google Colab environment, it automates the process of marking student attendance and simultaneously captures their dominant emotional state during the recognition.
## Features

*   **Automated Attendance**: Mark students present or absent based on real-time facial recognition.
*   **Emotion Analysis**: Detects the dominant emotion (e.g., happy, sad, angry, neutral) of recognized individuals.
*   **Google Drive Integration**: Utilizes Google Drive for storing student face databases and attendance logs, ensuring persistence and easy access.
*   **Real-time Camera Feed**: Captures images via webcam within the Colab environment.
*   **CSV Logging**: Maintains a detailed attendance log including date, time, student name, attendance status, and detected mood in a CSV file.
*   **Extendable**: Easy to add new students to the database.

## How It Works

1.  **Setup**: Mounts Google Drive and installs necessary libraries (`deepface`, `opencv`).
2.  **Student Database**: Scans a specified folder in Google Drive (`student_db`) where each subfolder represents a student and contains their facial images.
3.  **Real-time Capture**: Continuously captures images from the user's webcam.
4.  **Facial Recognition**: Uses DeepFace to compare captured faces against the student database.
5.  **Emotion Detection**: For recognized faces, DeepFace analyzes the dominant emotion.
6.  **Attendance Logging**: Records attendance and mood in a `attendance_log.csv` file, marking recognized students as 'Present' with their mood, and others as 'Absent'.
7.  **Visual Feedback**: Displays the captured image with recognition results overlayed.

## Getting Started

### Prerequisites

*   Google Colab account.
*   Access to a webcam.

### Setup Instructions

1.  **Open in Google Colab**: Click the "Open in Colab" badge (if you add one) or upload the notebook to Google Colab.
2.  **Mount Google Drive**: Run the first code cell to mount your Google Drive. This is crucial for accessing your student database and saving logs.
3.  **Install DeepFace**: The first cell also handles the installation of the `deepface` library and its dependencies.
4.  **Create Project Structure in Google Drive**:
    *   In your Google Drive, create a folder named `AI_Attendence`.
    *   Inside `AI_Attendence`, create another folder named `student_db`.
    *   For each student, create a subfolder within `student_db` (e.g., `student_db/Rimsha Abbas Khan`, `student_db/Muhammad Abbas Khan`).
    *   Place several clear images of each student (preferably from different angles and lighting) into their respective subfolders. These images will form the facial recognition database.
5.  **Run `take_photo` Function**: Execute the cell defining the `take_photo` function. This sets up the camera capture functionality.
6.  **Start Attendance System**: Run the cell containing `run_ai_attendance()`. This will initiate the webcam and the attendance process.

## Usage

Once the `run_ai_attendance()` function is executing:

*   A camera feed will appear in your Colab output.
*   Click the **"Capture Attendance"** button to take a photo. The system will then attempt to recognize faces and log attendance.
*   The results (recognized student, mood, attendance status) will be printed in the output, and the log will be updated in `attendance_log.csv`.
*   Continue clicking **"Capture Attendance"** for subsequent students or different captures.
*   Click the **"Done (Stop Camera)"** button to end the attendance session.
*   You can then view the complete `attendance_log.csv` using the provided code cell for displaying the log.

## Technologies Used

*   Python 3
*   Google Colab
*   DeepFace (for facial recognition and emotion analysis)
*   OpenCV (`cv2`) (for image processing)
*   Pandas (for data manipulation and CSV logging)
*   Google Drive API (for file storage)

## Contribution

Contributions are welcome! If you have suggestions or improvements, feel free to open an issue or submit a pull request.

