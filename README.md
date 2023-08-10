
# Flatmates Bill Calculator

This project is a Flask-based web application that calculates bill shares between flatmates and generates a PDF report with the calculated amounts.

## Features

- **Web Interface:** Users can enter bill details and flatmates' information through a user-friendly web interface.
- **Bill Calculation:** The app calculates each flatmate's share of the bill based on the number of days they stayed in the house.
- **PDF Report Generation:** The calculated bill shares are presented in a PDF report, including flatmates' names, due amounts, and the bill period.
- **File Sharing:** The PDF report is uploaded to the web, and a shareable link is generated for easy sharing.

## Usage

1. Install the required dependencies from the `requirements.txt` file:

   ```
   pip install -r requirements.txt
   ```

2. Run the Flask app:

   ```
   python main.py
   ```

3. Access the app by navigating to `http://127.0.0.1:5000` in your web browser.

## File Structure

```
- flatmates_bill/
  - main.py
  - flat.py
  - reports.py
  - static/
    - main.css
  - templates/
    - bill_form_page.html
    - index.html
    - results.html
  - files/
    - house.png
  - frontend.kv
  - filesharer.py
- requirements.txt
```

## Components

- **main.py:** Main entry point of the Flask application, handles routing and views.
- **flat.py:** Contains the `Bill` and `Flatmate` classes for bill calculations.
- **reports.py:** Includes the `PdfReport` and `FileSharer` classes for generating PDF reports and sharing files.
- **static/main.css:** CSS file for styling the web pages.
- **templates/:** HTML templates for the different web pages.
- **files/house.png:** Icon used in the PDF report.
- **frontend.kv:** Kivy language file for UI design.
- **filesharer.py:** FileSharer class for uploading files and generating shareable links.
- **requirements.txt:** Lists required packages for the project.

## Contributing

Contributions are welcome! If you have any suggestions or improvements, feel free to open an issue or submit a pull request.

## Credits

This project was inspired by a coding challenge and was developed by [Your Name].

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgements

Special thanks to the Kivy and Flask communities for their wonderful frameworks and libraries.

---
