# Advanced HTML5 Elements and Forms

## Objectives
Implement HTML5 images, lists, tables, forms and input types.
Use form validation attributes.
Apply multimedia elements such as audio and video.

## Instructions

- Create an index.html file.
- Add an ordered list with roman numerals
- Add an external image from pexels.com
- Add a table of 5 contacts with; name, address, mobile and emails
- Add a registration form

>[!NOTE]
>  The registration form should have:
>- Name, email, password, and date fields.
>- A dropdown, radio buttons, and checkboxes.
>- Proper labels and placeholders.
>- Required fields and validation attributes.
>- Ensure proper indentation and commenting.
 
# Tasks
- Create a well-structured HTML5 document.
- Ensure semantic correctness.

Happy Coding! 💻✨







<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Advanced HTML5 Elements and Forms</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        section {
            margin-bottom: 30px;
            padding: 20px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: left;
        }
        th {
            background-color: #f2f2f2;
        }
        form {
            max-width: 600px;
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        input, select, textarea {
            width: 100%;
            padding: 8px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <header>
        <h1>Advanced HTML5 Elements Demonstration</h1>
    </header>

    <!-- Ordered List with Roman Numerals -->
    <section id="ordered-list">
        <h2>Steps to Build a Website (Ordered List with Roman Numerals)</h2>
        <ol type="I">
            <li>Plan your website structure</li>
            <li>Create wireframes and mockups</li>
            <li>Write HTML markup</li>
            <li>Add CSS styling</li>
            <li>Implement JavaScript functionality</li>
            <li>Test across browsers and devices</li>
            <li>Deploy to a web server</li>
        </ol>
    </section>

    <!-- External Image from Pexels -->
    <section id="external-image">
        <h2>Beautiful Nature Image from Pexels</h2>
        <figure>
            <img src="https://images.pexels.com/photos/15286/pexels-photo.jpg" 
                 alt="Scenic mountain landscape with trees and fog" 
                 width="800"
                 height="500">
            <figcaption>Mountain landscape photo from Pexels.com</figcaption>
        </figure>
    </section>

    <!-- Contacts Table -->
    <section id="contacts-table">
        <h2>Contact List</h2>
        <table>
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Address</th>
                    <th>Mobile</th>
                    <th>Email</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>John Smith</td>
                    <td>123 Main St, Anytown, USA</td>
                    <td>(555) 123-4567</td>
                    <td>john.smith@example.com</td>
                </tr>
                <tr>
                    <td>Sarah Johnson</td>
                    <td>456 Oak Ave, Somewhere, USA</td>
                    <td>(555) 987-6543</td>
                    <td>sarah.j@example.com</td>
                </tr>
                <tr>
                    <td>Michael Brown</td>
                    <td>789 Pine Rd, Nowhere, USA</td>
                    <td>(555) 456-7890</td>
                    <td>m.brown@example.com</td>
                </tr>
                <tr>
                    <td>Emily Davis</td>
                    <td>321 Elm Blvd, Anywhere, USA</td>
                    <td>(555) 789-0123</td>
                    <td>emily.d@example.com</td>
                </tr>
                <tr>
                    <td>David Wilson</td>
                    <td>654 Maple Ln, Everywhere, USA</td>
                    <td>(555) 234-5678</td>
                    <td>dwilson@example.com</td>
                </tr>
            </tbody>
        </table>
    </section>

    <!-- Registration Form -->
    <section id="registration-form">
        <h2>Registration Form</h2>
        <form id="register" action="/submit" method="post" novalidate>
            <!-- Personal Information -->
            <div class="form-group">
                <label for="name">Full Name*</label>
                <input type="text" id="name" name="name" placeholder="Enter your full name" required minlength="3">
            </div>

            <div class="form-group">
                <label for="email">Email*</label>
                <input type="email" id="email" name="email" placeholder="Enter your email address" required>
            </div>

            <div class="form-group">
                <label for="password">Password*</label>
                <input type="password" id="password" name="password" placeholder="Create a password" 
                       required minlength="8" pattern="^(?=.*[A-Za-z])(?=.*\d)[A-Za-z\d]{8,}$"
                       title="Minimum 8 characters, at least one letter and one number">
            </div>

            <div class="form-group">
                <label for="dob">Date of Birth*</label>
                <input type="date" id="dob" name="dob" required>
            </div>

            <!-- Dropdown for Country -->
            <div class="form-group">
                <label for="country">Country*</label>
                <select id="country" name="country" required>
                    <option value="" disabled selected>Select your country</option>
                    <option value="US">United States</option>
                    <option value="CA">Canada</option>
                    <option value="UK">United Kingdom</option>
                    <option value="AU">Australia</option>
                    <option value="JP">Japan</option>
                    <option value="other">Other</option>
                </select>
            </div>

            <!-- Radio buttons for Gender -->
            <div class="form-group">
                <label>Gender</label>
                <div>
                    <input type="radio" id="male" name="gender" value="male">
                    <label for="male" style="display: inline;">Male</label>
                </div>
                <div>
                    <input type="radio" id="female" name="gender" value="female">
                    <label for="female" style="display: inline;">Female</label>
                </div>
                <div>
                    <input type="radio" id="other" name="gender" value="other">
                    <label for="other" style="display: inline;">Other</label>
                </div>
                <div>
                    <input type="radio" id="prefer-not-to-say" name="gender" value="prefer-not-to-say" checked>
                    <label for="prefer-not-to-say" style="display: inline;">Prefer not to say</label>
                </div>
            </div>

            <!-- Checkboxes for Interests -->
            <div class="form-group">
                <label>Interests (Select all that apply)</label>
                <div>
                    <input type="checkbox" id="technology" name="interests" value="technology">
                    <label for="technology" style="display: inline;">Technology</label>
                </div>
                <div>
                    <input type="checkbox" id="sports" name="interests" value="sports">
                    <label for="sports" style="display: inline;">Sports</label>
                </div>
                <div>
                    <input type="checkbox" id="music" name="interests" value="music">
                    <label for="music" style="display: inline;">Music</label>
                </div>
                <div>
                    <input type="checkbox" id="travel" name="interests" value="travel">
                    <label for="travel" style="display: inline;">Travel</label>
                </div>
            </div>

            <!-- Additional HTML5 input types -->
            <div class="form-group">
                <label for="phone">Phone Number</label>
                <input type="tel" id="phone" name="phone" placeholder="Enter your phone number" pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}">
                <small>Format: 123-456-7890</small>
            </div>

            <div class="form-group">
                <label for="website">Website (optional)</label>
                <input type="url" id="website" name="website" placeholder="https://example.com">
            </div>

            <div class="form-group">
                <label for="bio">Short Bio</label>
                <textarea id="bio" name="bio" rows="4" placeholder="Tell us about yourself"></textarea>
            </div>

            <!-- Terms and Conditions -->
            <div class="form-group">
                <input type="checkbox" id="terms" name="terms" required>
                <label for="terms" style="display: inline;">I agree to the terms and conditions*</label>
            </div>

            <!-- Submit Button -->
            <button type="submit">Register</button>
        </form>
    </section>

    <!-- Multimedia Section -->
    <section id="multimedia">
        <h2>Multimedia Elements</h2>
        
        <h3>Audio Example</h3>
        <audio controls>
            <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
            Your browser does not support the audio element.
        </audio>
        
        <h3>Video Example</h3>
        <video width="800" controls poster="https://images.pexels.com/photos/15286/pexels-photo.jpg">
            <source src="https://samplelib.com/lib/preview/mp4/sample-5s.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </section>

    <footer>
        <p>&copy; 2023 Advanced HTML5 Demo. All rights reserved.</p>
    </footer>
</body>
</html>
