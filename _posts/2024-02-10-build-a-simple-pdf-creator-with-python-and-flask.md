---
title: Build a simple PDF creator with Python and Flask
layout: post
categories:
- Python
- GitHub
image: assets/images/post/PDFcreator.jpg
tags: [Python,GitHub]
description: In this blog post, I've demonstrated how to create a simple web application
  using Python and Flask for converting files to PDF. This solution provides a user-friendly
  interface for uploading files and seamlessly converting them into PDF format. By
  harnessing the power of Python libraries like Flask and FPDF, we've simplified the
  process of file conversion, offering convenience and efficiency to users. Whether
  you're a student, professional, or business owner, having a tool like this at your
  disposal can streamline your document management tasks and enhance productivity.
  So why wait? Give it a try and experience the benefits of file to PDF conversion
  firsthand!
---

In today's digital age, the ability to convert files into different formats is crucial for various tasks. One common requirement is converting files to PDF, a widely used format for sharing documents while preserving their layout and formatting. In this blog post, we'll explore a simple solution using Python and Flask to create a web application that allows users to upload files and convert them to PDF effortlessly.


In this blog post, we'll delve use Python for building PDF creator.
# **Building the File to PDF Converter:**

Now, let's delve into the technical aspect of creating our file to PDF converter using Python and Flask.

**1. Setting Up the Environment:**
Ensure you have Python installed on your system. You can install Flask, a lightweight web framework for Python, using pip:

```
pip install Flask

```
**2. Creating the Web Application:**
We'll create a simple web application with Flask that allows users to upload files and convert them to PDF.

```
# Import necessary libraries
from flask import Flask, request, send_file
from werkzeug.utils import secure_filename
from fpdf import FPDF

app = Flask(__name__)

# Set the directory where uploaded files will be stored
UPLOAD_FOLDER = 'uploads'
app.config['UPLOAD_FOLDER'] = UPLOAD_FOLDER

# Function to convert the uploaded file to PDF
def convert_to_pdf(file_path):
    pdf = FPDF()
    pdf.add_page()
    pdf.set_font("Arial", size = 12)
    with open(file_path, 'rb') as f:
        for line in f:
            pdf.cell(200, 10, txt=line.decode('latin-1'), ln=True)
    pdf_file_path = file_path.rsplit('.', 1)[0] + '.pdf'
    pdf.output(pdf_file_path)
    return pdf_file_path

@app.route('/')
def index():
    return '''<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>File to PDF Converter</title>
</head>
<body>
    <h1>File to PDF Converter</h1>
    <form action="/upload" method="post" enctype="multipart/form-data">
        <input type="file" name="file">
        <button type="submit">Upload & Convert to PDF</button>
    </form>
</body>
</html>'''

@app.route('/upload', methods=['POST'])
def upload_file():
    if 'file' not in request.files:
        return 'No file part'
    file = request.files['file']
    if file.filename == '':
        return 'No selected file'
    if file:
        filename = secure_filename(file.filename)
        file_path = os.path.join(app.config['UPLOAD_FOLDER'], filename)
        file.save(file_path)
        pdf_file_path = convert_to_pdf(file_path)
        return send_file(pdf_file_path, as_attachment=True)
    return 'Error uploading file'

if __name__ == '__main__':
    app.run(debug=True)

```


In this blog post, I've demonstrated how to create a simple web application using Python and Flask for converting files to PDF. This solution provides a user-friendly interface for uploading files and seamlessly converting them into PDF format. By harnessing the power of Python libraries like Flask and FPDF, we've simplified the process of file conversion, offering convenience and efficiency to users. Whether you're a student, professional, or business owner, having a tool like this at your disposal can streamline your document management tasks and enhance productivity. So why wait? Give it a try and experience the benefits of file to PDF conversion firsthand!
