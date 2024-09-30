# Resume Categorization Web Application

## Overview

This web application allows users to upload resumes in PDF or TXT format, extract relevant information, and predict the category of the resume using machine learning. The application utilizes pre-trained models to classify resumes and extract data such as contact details, skills, education, and names.

## Features

- **Resume Upload**: Upload resumes in PDF or TXT format.
- **Category Prediction**: Classifies the resume into predefined categories using a Random Forest classifier.
- **Data Extraction**: Extracts contact numbers, emails, skills, education, and names from the resume.
- **User-friendly Interface**: Simple and intuitive web interface for easy interaction.

## Technologies Used

- **Flask**: Lightweight web framework for building the application.
- **scikit-learn**: Machine learning library for model creation and prediction.
- **PyPDF2**: Library for extracting text from PDF files.
- **pickle**: For loading serialized machine learning models.
- **Regular Expressions (re)**: For text processing and data extraction.

## Requirements

- Python 3.x
- Flask
- scikit-learn
- PyPDF2

## Installation

1. **Clone the repository**:
    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. **Install the required packages**:
    ```bash
    pip install Flask scikit-learn PyPDF2
    ```

3. **Download necessary model files**:
   Ensure `clf.pkl` and `tfidf.pkl` are present in the project directory. These files contain the trained classifier and vectorizer.

## Usage

1. **Run the application**:
    ```bash
    python app.py
    ```

2. **Access the application**:
   Open your web browser and navigate to `http://127.0.0.1:5000/`.

3. **Upload a resume**:
   Use the interface to upload a PDF or TXT resume. The application will process the file and display the results, including the predicted category and extracted information.

## API Endpoints

- **GET /**: Renders the main upload page.
- **POST /pred**: Accepts the uploaded resume file, processes it, and returns the predicted category and extracted information.

## Extracted Information

Upon processing a resume, the following information will be displayed:

- **Predicted Category**: The predicted classification of the resume.
- **Contact Number**: Extracted phone number.
- **Email**: Extracted email address.
- **Skills**: List of identified skills.
- **Education**: Educational qualifications extracted.
- **Name**: Candidate's name extracted from the resume.

## Example Skills and Education Keywords

The application contains predefined lists of skills and education keywords, which can be modified in the code as needed.

## Contributing

Feel free to submit issues or pull requests. Contributions are welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Note

Test the application with various resume formats and structures to ensure robustness in data extraction and classification.
