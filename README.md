# Photovoltaic-System

![architecture](https://github.com/user-attachments/assets/39578d19-f6c8-4445-a107-86d8c25d40f5)


## Overview

The project is to create a **web-based photovoltaic system calculation tool** that provides better planning options for photovoltaic systems. The tool will use **current weather data** and **local conditions** to estimate the usability and effectiveness of photovoltaic systems from a particular manufacturer and product. The final product will include both a **term paper** and a **working web-based prototype**.

## Task Requirements

### Term Paper
- **Content**: Around 6 pages excluding cover, appendix, and bibliography.
- **Form**: Balanced ratio of text and pictures (relevant screenshots should be referred to in the text).
- **Technologies**: Provide an overview of all used technologies (DBMS, programming languages, frameworks, APIs) and justify their use.
- **Project Description**: The term paper should describe the entire project, including functionalities, without requiring execution.
- **References**: Cite all used sources, libraries, and technologies.
- **API Documentation**: The appendix should include a complete web service API documentation with endpoints, parameters, return values, and status codes.

### Programming Tasks

#### Database
1. **Data Storage**: All data must be stored in a database, except for configuration data and temporary storage that is cleaned up after use.
2. **Frontend-Backend Communication**: The frontend should never communicate directly with the database.

#### Backend
1. **Data Processing**: The backend handles all data processing and communication with the database.
2. **Weather Data**: Fetch live weather data from external APIs. Scrape weather data periodically via a cron job.
3. **Email Reports**: Backend should handle the sending of emails with system reports.

#### Web Service API
1. Provide a web service API to communicate between the frontend, backend, and database.
2. Catch API access failures and return appropriate error messages and HTTP status codes.

#### Frontend UI
1. **Web Application**: Accessible via common web browsers (e.g., Firefox, Safari, Chromium-based browsers).
2. **Responsive Design**: The application must support various devices, screen sizes, and orientations.
3. **Usability**: Intuitive design with minimal user interaction required to perform tasks.
4. **User Account**: Users can create, update, and delete accounts. Each user has a profile page.
5. **Projects**: Users can create, update, and delete photovoltaic system projects.
6. **Products**: Users can choose from predefined photovoltaic system products and specify multiple products for each project.
7. **Visualization**: Display locations of photovoltaic systems on a map and generate reports showing electricity production based on weather data.
8. **Report Generation**: Automatically generate a report after 30 days or trigger it manually. The report is based on 6 parameters: Power peak, orientation, inclination, area, longitude, latitude.
9. **Read-Only Projects**: After report generation, projects become read-only.
10. **Chart/Diagram**: Visualize electricity output with charts/diagrams.

### Additional Group Tasks
- **Sync Weather Data**: Provide an option for users to manually sync weather data in addition to the automatic cron job.
- **Company Accounts**: Companies can create, update, and delete their accounts and photovoltaic products.
- **User Types**: Implement two types of users: free (limited to 1 project) and unlimited users.
- **Authentication Layer**: Implement API authentication (e.g., JWT, OAuth).
- **Report Customization**: Allow users to choose the report date range (up to 1 year) with a default of 30 days.
- **Password Encryption**: Encrypt user passwords.
- **Soft Delete**: Implement soft deletion for user accounts.
- **PV/Watts Calculation**: Add more parameters (e.g., clouds and system loss) to the electricity calculation.
- **Location Input**: Convert user-provided locations into latitude and longitude for the photovoltaic system.

## Evaluation
- **Presentation**: 15-minute presentation with a live demonstration of the project features.
- **Examination**: Questions on the project, term paper, and course content.

## License
This project is licensed under the [MIT License](https://github.com/SamiAlavi/Photovoltaic-System/blob/main/LICENSE).
