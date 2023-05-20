# IREPORT APPLICATION

## Application Overview

Ireport is an application designed to facilitate communication between citizens and authorities regarding potential issues in their community. With Ireport, users can easily post redflags or interventions related to things like public safety, infrastructure, or other concerns. The platform allows users to provide detailed information about the issue, including photos and location data. Once posted, the relevant authorities can view and respond to these reports, allowing for swift and effective resolution of problems. Ireport is a powerful tool for promoting transparency and accountability, and helps to foster greater collaboration between citizens and their government.

## Setup and Installation

1. ***Clone the repository:*** Open a terminal window and navigate to the directory where you want to download the application.

2. ***Install dependencies:*** Navigate to the project directory and install the dependencies for both the backend (Ruby on Rails) and frontend (ReactJS).
cd to the backend and frontend on separate terminals respectively.
For the backend, use the following command to install the required gems:

```javascript
   bundle install
   ```
For the frontend, use the following command to install the required packages:

```javascript
   cd client
   npm install
 ```
 3. ***Set up the database:*** In the terminal window, navigate to the project directory and run the following commands to create and migrate the database:

  ```ruby
   rails db:create
   rails db:migrate
   ```
 4. ***Start the server:*** In the terminal window, navigate to the project directory and run the following command to start the server:

 ```ruby
   rails s
 ```
 5. ***Start the client:*** In a new terminal window, navigate to the project directory and run the following command to start the frontend server:
   ```javascript
   cd client
   npm start

   ```
 6. ***Access the application:*** Open a web browser and navigate to http://localhost:3000 to access the application.


 
                ```

## Application Usage

Open the application in your web browser by navigating to the URL where it is hosted.
as a user you can sign-up and login to your account and view a list of all public reports.
To post a report, click on the **"Report Now"** button on the **Homepage** or the **Add Report** button on the **"Navigation bar"**. This will bring up a form where you can enter the details of your report, including the type of report (red flag or intervention), the location, and a description of the issue. Once you have filled out the form, click the **"Submit"** button to post the report.

***Report to hold individuals accountable, prevent harm, protect communities, and create a fair society.***

As an admin, you can update the status of a report by following these steps:

Log in to the application with your admin credentials.
Navigate to the homepage or dashboard where you can see a list of all the reports.
Click on the report you want to update. This will take you to the report details page.
On the report details page, locate the report status field. It may be labeled as "Current Status" or something similar.
Select the new status for the report from the dropdown menu. The available options may include "Under Investigation," "Rejected," or "Resolved". 
Click the "Update" or "Save" button to save the changes and update the report status.

## Technologies Used

1. Programming Languages: JavaScript, Ruby

2. Frontend Frameworks/Libraries: React

3. Backend Frameworks/Libraries: Ruby on Rails

4. Database Management Systems: PostgreSQL

5. Version Control: Git, GitHub

6. Other Libraries and Tools: TailwindCSS

## Backend API Documentation

The backend of the Ireporter application is built with Ruby on Rails and provides several API endpoints for managing reports. Below is the documentation for each endpoint, including details on the request and response formats.

### GET /reports

Description

Retrieves a list of all reports.

_Request_

HTTP Method: GET
Endpoint: /reports
Response Body: List of reports in JSON format


_Response_

Status: 200 OK
Body: JSON formatted list of all reports


### GET /reports/:id

Description
Retrieves a specific report by its ID.

_Request_

HTTP Method: GET
Endpoint: /reports/:id
Response Body: The specified report in JSON format

_Response_

Status: 200 OK
Body: JSON formatted report

### POST /reports

Description
Creates a new report with the provided parameters.

_Request_

HTTP Method: POST
Endpoint: /reports
Request Body: JSON formatted report parameters



| Field              | Type    | Description                                       |
| :-----------------| :------| :-------------------------------------------------|
| description        | string  | Description of the report                         |
| image              | string  | URL of the image attached to the report           |
| video              | string  | URL of the video attached to the report           |
| gps_coordinates    | string  | GPS coordinates of the report                     |
| user_id            | integer | ID of the user who created the report             |
| report_type_id     | integer | ID of the report type                             |
| report_status_id   | integer | ID of the report status                           |
| title              | string  | Title of the report                                |
| location_name      | string  | Name of the location associated with the report   |


_Response_

Status: 201 Created
Body: JSON formatted report

### PATCH/PUT /reports/:id
Description
Updates an existing report with the provided parameters.

Request
HTTP Method: PATCH/PUT
Endpoint: /reports/:id
Request Body: JSON formatted report parameters

| Field            | Type    | Description                                          |
| :-----------------|:---------|:------------------------------------------------------|
| description     | string  | Description of the report                            |
| image           | string  | URL of the image attached to the report              |
| video           | string  | URL of the video attached to the report              |
| gps_coordinates | string  | GPS coordinates of the report                        |
| user_id         | integer | ID of the user who created the report                |
| report_type_id  | integer | ID of the report type                                 |
| report_status_id| integer | ID of the report status                               |
| title           | string  | Title of the report                                   |
| location_name   | string  | Name of the location associated with the report       |


_Response_

Status: 202 Accepted
Body: JSON formatted report


### DELETE /reports/:id
Description
Deletes the specified report.

_Request_

HTTP Method: DELETE
Endpoint: /reports/:id


_Response_

Status: 202 No Content

### GET /users/:user_id/reports

Description
Retrieves a list of reports belonging to a specific user.

_Request_

HTTP Method: GET
Endpoint: /users/:user_id/reports
Response Body: List of reports belonging to the specified user in JSON format

_Response_

Status: 200 OK
Body: JSON formatted list of user-specific reports

   ### Request Body Parameters

   | Field           | Type    | Description                                        |
| :------------- | :----- | :------------------------------------------------- |
| description    | string  | Description of the report                          |
| image          | string  | URL of the image attached to the report            |
| video          | string  | URL of the video attached to the report            |
| gps_coordinates| string  | GPS coordinates of the report                      |

## Front-End Documentation

The front-end of the application was built using HTML, CSS, and JavaScript, along with the following external libraries and frameworks:

1. React.js v18
2. Tailwind CSS


### Running the Application Locally

To run the front-end of the application locally, follow these steps:

Clone the repository to your local machine
Navigate to the frontend directory
Install the dependencies using npm install
Start the application using npm start
The application should now be running on http://localhost:3000/

## Conclusion

In conclusion, the Ireporter application provides a platform for users to report incidents anonymously or with their identities while allowing them to attach relevant media files and location data. The application's functionality includes creating, reading, updating, and deleting reports. With the front-end code stored in the /src folder and the index.html file stored in the /public folder, the application is easily accessible through a web browser. The back-end code handles the logic for the report controllers and can store and retrieve data from a database. Overall, the Ireporter application is a simple and effective solution for users to report incidents in a streamlined and efficient way.
