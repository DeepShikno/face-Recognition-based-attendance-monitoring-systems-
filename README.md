# Face Recognition-Based Attendance Monitoring System

A Python desktop application that marks attendance automatically using real-time face recognition. It has a simple Tkinter GUI, so non-technical users can register people and take attendance from a webcam without touching code.

## Features

- **Real-time face recognition:** detects and identifies faces from a webcam feed using OpenCV's LBPH recognizer.
- **Easy-to-use GUI:** the whole interface is built with Tkinter.
- **Password-protected registration:** only authorized users can register new people or change the password.
- **Student details management:** creates and updates a CSV file (`StudentDetails.csv`) when a new person is registered.
- **Daily attendance logs:** automatically creates a new CSV file each day (for example `Attendance_27-11-2025.csv`) with ID, name, date, and timestamp.
- **Live attendance view:** shows the day's attendance on the main screen in table form, updated as people are recognized (Pandas).

## Tech Stack

| Area | Tools |
|---|---|
| Language | Python 3 |
| GUI | Tkinter |
| Face detection & recognition | OpenCV (`cv2.face.LBPHFaceRecognizer_create()`) |
| Data handling | Pandas, NumPy, CSV, datetime |

## How It Works

1. **Register:** enter the ID and name (password required), and the app captures face images from the webcam.
2. **Train:** the captured images are used to train the LBPH recognizer.
3. **Take attendance:** the webcam identifies each face, and the app records the ID, name, date, and time in that day's CSV file.
4. **Review:** the main screen displays the attendance recorded so far, and the CSV files can be opened in Excel or any spreadsheet tool.

## Getting Started

### Prerequisites

- Python 3.8 or later
- A working webcam

### Installation

```bash
git clone https://github.com/DeepShikno/face-Recognition-based-attendance-monitoring-systems-.git
cd face-Recognition-based-attendance-monitoring-systems-
pip install opencv-contrib-python numpy pandas pillow
```

> `opencv-contrib-python` is required because the LBPH recognizer lives in OpenCV's contrib module.
> See `install commands .txt` in this repo for the original setup notes.

### Run

```bash
python main.py
```



<!-- TODO: if this project is based on another developer's open-source work, credit them here with a link
     to the original repository, and keep the LICENSE file. -->

## License

See the [LICENSE](LICENSE) file for details.
