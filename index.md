 Assignment 4.2 — Job Application Form
 1. HTML code — job-application.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Job Application Form</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #f0f4f8;
            margin: 0;
            padding: 30px 15px;
        }

        .container {
            max-width: 600px;
            margin: auto;
            background-color: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }

        h2 {
            text-align: center;
            color: #2563eb;
            margin-bottom: 25px;
        }

        .form-group {
            margin-bottom: 18px;
        }

        label {
            display: block;
            font-weight: bold;
            margin-bottom: 8px;
            color: #333;
        }

        input:not([type="radio"]):not([type="checkbox"]),
        select,
        textarea {
            width: 100%;
            padding: 11px;
            border: 1px solid #ccc;
            border-radius: 6px;
            font-size: 15px;
        }

        input:focus,
        select:focus,
        textarea:focus {
            outline: none;
            border-color: #2563eb;
        }

        .option {
            margin: 8px 0;
        }

        .option label {
            display: inline;
            font-weight: normal;
            margin-left: 5px;
        }

        input[type="radio"],
        input[type="checkbox"] {
            accent-color: #2563eb;
        }

        input:disabled {
            background-color: #e5e7eb;
            color: #777;
            cursor: not-allowed;
        }

        textarea {
            resize: vertical;
        }

        button {
            width: 100%;
            padding: 13px;
            background-color: #2563eb;
            color: white;
            border: none;
            border-radius: 6px;
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background-color: #1d4ed8;
        }

        #message {
            text-align: center;
            color: green;
            margin-top: 15px;
        }
    </style>
</head>

<body>

    <div class="container">
        <h2>Job Application Form</h2>

        <form id="jobForm">

            <div class="form-group">
                <label for="fullName">Full Name:</label>
                <input
                    type="text"
                    id="fullName"
                    name="fullName"
                    placeholder="Enter your full name"
                    required
                >
            </div>

            <div class="form-group">
                <label for="email">Email Address:</label>
                <input
                    type="email"
                    id="email"
                    name="email"
                    placeholder="Enter your email"
                    required
                >
            </div>

            <div class="form-group">
                <label for="phone">Phone Number:</label>
                <input
                    type="tel"
                    id="phone"
                    name="phone"
                    placeholder="Enter your phone number"
                    required
                >
            </div>

            <div class="form-group">
                <label for="dob">Date of Birth:</label>
                <input
                    type="date"
                    id="dob"
                    name="dob"
                    required
                >
            </div>

            <div class="form-group">
                <label for="portfolio">Portfolio URL:</label>
                <input
                    type="url"
                    id="portfolio"
                    name="portfolio"
                    placeholder="https://example.com"
                    required
                >
            </div>

            <div class="form-group">
                <label>Preferred Shift:</label>

                <div class="option">
                    <input
                        type="radio"
                        id="morning"
                        name="shift"
                        value="Morning"
                        required
                    >
                    <label for="morning">Morning</label>
                </div>

                <div class="option">
                    <input
                        type="radio"
                        id="evening"
                        name="shift"
                        value="Evening"
                    >
                    <label for="evening">Evening</label>
                </div>

                <div class="option">
                    <input
                        type="radio"
                        id="night"
                        name="shift"
                        value="Night"
                    >
                    <label for="night">Night</label>
                </div>
            </div>

            <div class="form-group">
                <label>Skills:</label>

                <div class="option">
                    <input
                        type="checkbox"
                        id="html"
                        name="skills"
                        value="HTML"
                    >
                    <label for="html">HTML</label>
                </div>

                <div class="option">
                    <input
                        type="checkbox"
                        id="css"
                        name="skills"
                        value="CSS"
                    >
                    <label for="css">CSS</label>
                </div>

                <div class="option">
                    <input
                        type="checkbox"
                        id="javascript"
                        name="skills"
                        value="JavaScript"
                    >
                    <label for="javascript">JavaScript</label>
                </div>

                <div class="option">
                    <input
                        type="checkbox"
                        id="python"
                        name="skills"
                        value="Python"
                    >
                    <label for="python">Python</label>
                </div>
            </div>

            <div class="form-group">
                <label for="qualification">Highest Qualification:</label>

                <select
                    id="qualification"
                    name="qualification"
                    required
                >
                    <option value="">-- Select Qualification --</option>
                    <option value="High School">High School</option>
                    <option value="Diploma">Diploma</option>
                    <option value="Bachelor's Degree">Bachelor's Degree</option>
                    <option value="Master's Degree">Master's Degree</option>
                    <option value="PhD">PhD</option>
                </select>
            </div>

            <div class="form-group">
                <label for="coverLetter">Cover Letter:</label>

                <textarea
                    id="coverLetter"
                    name="coverLetter"
                    rows="5"
                    placeholder="Write a short cover letter..."
                    required
                ></textarea>
            </div>

            <div class="form-group">
                <label for="applicationId">Application ID (Disabled):</label>

                <input
                    type="text"
                    id="applicationId"
                    name="applicationId"
                    value="Assigned by HR"
                    disabled
                >
            </div>

            <button type="submit">Submit Application</button>

            <p id="message" role="status"></p>

        </form>
    </div>

    <script>
        const form = document.getElementById("jobForm");
        const message = document.getElementById("message");

        form.addEventListener("submit", function(event) {
            event.preventDefault();

            message.textContent =
                "Your job application has been submitted successfully!";

            form.reset();
        });
    </script>

</body>
</html>
2. How to run the assignment
Open Notepad or Visual Studio Code.

Copy and paste the entire code above.

Save the file as job-application.html.

Open the file in Google Chrome or another web browser.

Fill in the required fields, select a shift, choose your skills, and click Submit Application to test it.

3. Form preview
Job Application Form
Full Name:

Enter your full name

Email Address:

Enter your email

Phone Number:

Enter your phone number

Date of Birth:

Select date

Portfolio URL:

https://example.com

Preferred Shift:

◯ Morning

◯ Evening

◯ Night

Skills:

☐ HTML

☐ CSS

☐ JavaScript

☐ Python

Highest Qualification:

-- Select Qualification --

Cover Letter:

Write a short cover letter...

Application ID (Disabled):

Assigned by HR

Submit Application

This is an illustrative preview of the expected layout, not an actual screenshot of the running HTML file.
4. Checklist of assignment requirements
Requirement

Completed

Full name, email, phone

Yes

Date input for date of birth

Yes

URL input for portfolio

Yes

Radio buttons with the same name

Yes — shift

Skill checkboxes

Yes

Qualification dropdown

Yes

Cover letter <textarea>

Yes

Submit button

Yes

Labels and unique IDs

Yes

Required fields

Yes

Disabled field

Yes

5. Files to submit
job-application.html — your complete HTML form.

job-application-screenshot.png — screenshot of the form opened in your browser.