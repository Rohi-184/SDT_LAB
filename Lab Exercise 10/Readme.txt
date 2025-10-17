Exercise 10 Terminal commands :
---------------------------------------------------

docker --version ( To check Docker Version )


docker start my_httpd ( Start the container )


docker exec -it my_httpd/bin/bash ( Execute the bash shell )


cd htdocs ( Change directory to htdocs )


apt update ( update the apt installer )


apt install nano ( Install nano editor )


nano index.html ( Open the index.html )


( Replace the code on the index.html ) :

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #e0f7fa; /* Light blue background */
            padding: 20px;
        }
        .form-container {
            background: #ffffff; /* White background for the form */
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            max-width: 400px;
            margin: auto;
        }
        .form-group {
            margin-bottom: 15px;
        }
        .form-group label {
            display: block;
            margin-bottom: 5px;
        }
        .form-group input,
        .form-group select {
            width: 100%;
            padding: 8px;
            box-sizing: border-box;
        }
        .form-group button {
            width: 100%;
            padding: 10px;
            background: #28a745;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .form-group button:hover {
            background: #218838;
        }
    </style>
</head>
<body>

<div class="form-container">
    <h2>Registration Form</h2>
    <form action="#" method="post">
        <div class="form-group">
            <label for="name">Name:</label>
            <input type="text" id="name" name="name" required>
        </div>
        <div class="form-group">
            <label for="dob">Date of Birth:</label>
            <input type="date" id="dob" name="dob" required>
        </div>
        <div class="form-group">
            <label for="blood-group">Blood Group:</label>
            <select id="blood-group" name="blood_group" required>
                <option value="">Select Blood Group</option>
                <option value="A+">A+</option>
                <option value="A-">A-</option>
                <option value="B+">B+</option>
                <option value="B-">B-</option>
                <option value="AB+">AB+</option>
                <option value="AB-">AB-</option>
                <option value="O+">O+</option>
                <option value="O-">O-</option>
            </select>
        </div>
        <div class="form-group">
            <label>Gender:</label>
            <input type="radio" id="male" name="gender" value="Male" required>
            <label for="male">Male</label>
            <input type="radio" id="female" name="gender" value="Female" required>
            <label for="female">Female</label>
            <input type="radio" id="other" name="gender" value="Other" required>
            <label for="other">Other</label>
        </div>
        <div class="form-group">
            <label for="department">Department Name:</label>
            <input type="text" id="department" name="department" required>
        </div>
        <div class="form-group">
            <label for="college">College Name:</label>
            <input type="text" id="college" name="college" required>
        </div>
        <div class="form-group">
            <label for="father-name">Father's Name:</label>
            <input type="text" id="father-name" name="father_name" required>
        </div>
        <div class="form-group">
            <label for="mother-name">Mother's Name:</label>
            <input type="text" id="mother-name" name="mother_name" required>
        </div>
        <div class="form-group">
            <label for="city">City:</label>
            <input type="text" id="city" name="city" required>
        </div>
        <div class="form-group">
            <label for="mobile">Mobile No:</label>
            <input type="tel" id="mobile" name="mobile_no" required pattern="[0-9]{10}" title="Please enter a valid 10-digit mobile number">
        </div>
        <div class="form-group">
            <button type="submit">Register</button>
        </div>
    </form>
</div>

</body>
</html>



press Ctrl+o , Enter , Ctrl+x ( To Save & Exit the nano editor )


http://localhost:4567 ( On chrome browser to view web page )




