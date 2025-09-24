Infra-Alert: Real-Time Power Line Fault Detection
Infra-Alert is a single-page web application designed for the real-time monitoring, detection, and geospatial visualization of power line faults. It provides a comprehensive dashboard for operators to track grid health, analyze historical data, simulate fault scenarios, and leverage AI for predictive insights.

This project is built as a single, self-contained index.html file, making it extremely portable and easy to run locally without any build steps. For a more scalable version with a separate backend for AI prompt management (ideal for Google AI Studio), please see the project's commit history.

Key Features
Real-Time Event Feed: A live feed on the main dashboard displays new fault events as they are detected by the automated simulator.

Historical Data Analysis: View and search through a complete 8-month history of fault events. The dashboard also highlights faults that have occurred in the last 24 hours.

Geospatial Visualization: An interactive Google Map displays the entire power grid, plotting the precise geographical location of all detected faults, color-coded by severity. A "Show on Map" button for each historical fault provides a direct visual link.

AI-Powered Insights (Simulated):

Fault Summaries: Generate instant, human-readable summaries for any fault event.

Predictive Forecasting: Use AI to analyze all grid data and predict which power line is most vulnerable to a future fault.

Interactive Simulator: Manually trigger fault events on any power line to test system response or for demonstration purposes.

Getting Started
Prerequisites
You only need a modern web browser (like Chrome, Firefox, or Edge).

Running Locally
Download the File: Download the index.html file to your local machine.

Open the File: Simply open the index.html file in your web browser. The application will start immediately, with the real-time simulator beginning to generate new fault events.

Configuring the Google Maps API
The geospatial map view requires a Google Maps Platform API key with the Maps JavaScript API and Geometry Library enabled.

Get an API Key: Follow the instructions on the Google Cloud Console to create a project and get an API key.

Add the Key: Open the index.html file in a text editor and find the following line:

const GOOGLE_MAPS_API_KEY = "YOUR_GOOGLE_MAPS_API_KEY"; // <-- PASTE YOUR KEY HERE

Replace the Placeholder: Replace "YOUR_GOOGLE_MAPS_API_KEY" with your actual API key.

Save and Reload: Save the index.html file and refresh it in your browser. The map should now load correctly.

Project Structure
This entire application is contained within a single index.html file. This design choice simplifies distribution and setup.

HTML: Defines the structure and layout of the application.

Tailwind CSS: Used for all styling and is loaded via a CDN.

Chart.js: Used for data visualizations (donut charts) and is loaded via a CDN.

JavaScript: All application logic, including the real-time simulation, data management, and UI interactions, is contained within <script> tags at the bottom of the file. The AI features are currently simulated to allow the app to run without a backend, but can be connected to a serverless function.

This self-contained approach means there are no external dependencies to manage or build processes to run.