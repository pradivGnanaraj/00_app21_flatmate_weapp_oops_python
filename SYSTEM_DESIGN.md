**System Design: Flatmates Bill Calculator**

The "Flatmates Bill Calculator" is a web application designed to simplify the process of sharing bills among flatmates. Here's a system design outline for the application:

**1. High-Level Architecture:**

The application follows the client-server architecture, where the client (web browser) interacts with the server (Flask application) to manage and calculate bill sharing among flatmates.

**2. Components:**

- **Web Browser:** The client-side interface where users input bill details, view results, and interact with the application.

- **Flask Application (Server):** The backend logic of the application, handling user requests, calculations, and generating reports.
  
  - **app.py:** Main application file containing the Flask app configuration and routes.
  
  - **views.py:** Contains class-based views using Flask's MethodView for different application pages.
  
  - **forms.py:** Defines the WTForms for the bill input form.
  
  - **flatmates_bill/flat.py:** Contains the logic for calculating individual payments based on stay duration.
  
  - **flatmates_bill/reports.py:** Manages PDF report generation and file sharing.
  
  - **static/main.css:** Stylesheet for the frontend.
  
  - **templates/:** Contains HTML templates for different pages.
  
  - **files/:** Holds generated PDF reports and other shared files.
  
**3. User Interaction Flow:**

- User visits the homepage ("/") and selects the "Calculate Bill" option.
- User is redirected to the bill input form page ("/bill_form").
- User enters bill details, including amount, period, flatmate names, and their respective stay durations.
- Upon submission, the data is sent to the server for processing.
- The server calculates the fair share for each flatmate and generates a PDF report.
- The server provides a shareable link for the generated PDF report.
- User is redirected to the results page ("/results") where they can see the calculated amounts and shareable link.
- User can copy the link to the clipboard or open it in a browser.

**4. External Dependencies:**

- **Flask:** Web framework for handling requests, views, and routing.
- **WTForms:** For creating and handling the bill input form.
- **filestack:** Library for uploading and sharing files.
- **fpdf:** For generating PDF reports.
- **Pillow:** Python Imaging Library (PIL) for working with images.
- **webbrowser:** For opening URLs in the default browser.

**5. Deployment:**

The application can be deployed on a web server or cloud platform (such as Heroku or AWS) with the necessary configurations.

**6. Security Considerations:**

- Implement input validation to prevent potential security vulnerabilities.
- Use environment variables for sensitive data like API keys.
- Protect against cross-site scripting (XSS) attacks.
- Secure file uploads to prevent unauthorized access to files.

**7. Future Enhancements:**

- User authentication and accounts for storing historical data.
- Real-time notifications for bill calculations.
- Improved UI/UX design for better user experience.
- Integration with payment gateways for direct bill settlement.

The "Flatmates Bill Calculator" provides an efficient solution for flatmates to distribute bills fairly and generate shareable reports, making it a valuable tool for individuals sharing living expenses.