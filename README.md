# Textractor

This Python script utilizes the Tkinter library to create a graphical user interface (GUI) for performing Optical Character Recognition (OCR) on images using AWS Textract. Here's a breakdown of the project:

1. **Imports**: The script imports necessary modules such as Tkinter for GUI, filedialog for opening files, Pillow (PIL) for image processing, boto3 for AWS services, cv2 for OpenCV operations on images, http.client for HTTP connections, requests for making HTTP requests, io for working with file streams, and json for JSON manipulation.

2. **GUI Setup**: The Tkinter GUI is initialized with a title, dimensions, and an icon. Labels and buttons are created with appropriate text, fonts, and commands.

3. **Image Upload**: When the "Upload Image" button is clicked, a file dialog opens, allowing the user to select an image file (PNG or JPG). The selected image is then displayed on the GUI using Pillow's ImageTk.PhotoImage after resizing it to fit a specified dimension.

4. **OCR Functionality**: When the "Get Text" button is clicked, the `ocr()` function is triggered. This function performs OCR on the selected image using AWS Textract. First, the image is read using OpenCV (`cv2.imread()`). Then, the image is compressed and converted into bytes format suitable for HTTP transmission. An HTTP POST request is made to the OCR.Space API endpoint with the image data and API key. The response containing the extracted text is parsed from JSON, and the text is displayed on the GUI.

5. **Displaying Output**: The extracted text is displayed in a Label widget on the GUI.

6. **Main Loop**: The `root.mainloop()` function starts the Tkinter event loop, allowing the GUI to be interactive.

This project provides a simple interface for users to upload images and extract text from them using AWS Textract's OCR capabilities.
