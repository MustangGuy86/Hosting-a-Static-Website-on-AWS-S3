## Creating a Static Website and Hosting on Amazon S3

## Step1: Creating Website Files:

1.1. **HTML Script (index.html):**
   - Create a file named `index.html` in your project folder.
   - Open it with a text editor.
   - Add the HTML structure and content for your website. For example:
     ```html
     <!DOCTYPE html>
     <html>
     <head>
         <title>My Static Website</title>
         <link rel="stylesheet" type="text/css" href="style.css">
     </head>
     <body>
         <h1>Welcome to My Website</h1>
         <p>This is a static website hosted on Amazon S3.</p>
         <script src="script.js"></script>
     </body>
     </html>
     ```

1.2. **CSS Script (style.css):**
   - Create a file named `style.css` in your project folder.
   - Open it with a text editor.
   - Add CSS styles for your website. For example:
     ```css
     body {
         font-family: Arial, sans-serif;
         background-color: #f0f0f0;
     }
     h1 {
         color: #333;
     }
     ```

1.3. **JavaScript Script (script.js):**
   - Create a file named `script.js` in your project folder.
   - Open it with a text editor.
   - Add JavaScript code for any dynamic functionality. For example:
     ```javascript
     window.onload = function() {
         alert("Welcome to My Website!");
     };
     ```

Step 2: Create an S3 Bucket
In this step, you will create an S3 bucket to host your static website files.

2.1. Open AWS Management Console
Access the AWS Management Console.
Sign in with your AWS account credentials.
2.2. Navigate to S3
Find "S3" in the AWS Management Console or locate it under the "Storage" section.
Click on "S3" to open the S3 dashboard.
2.3. Create a New Bucket
Click the "Create bucket" button.
Configure the bucket with a unique name, region, and uncheck the option for "Block all public access."
Click the "Create bucket" button.
Step 3: Upload Website Files to S3
In this step, you will upload your HTML, CSS, and JavaScript files to the S3 bucket.

2.4. Open Your Bucket
In the S3 dashboard, click on the name of the bucket you just created.
2.5. Upload Files
Click the "Upload" button.
Add the HTML, CSS, and JavaScript files from your local folder.
Click the "Upload" button to upload the files.
2.6. Make Files Public
Select the uploaded HTML, CSS, and JavaScript files.
Click "Actions" and choose "Make public."
2.7. Individual Scripts

Make sure that the CSS and JavaScript files are also set to public access individually by selecting each file and choosing "Make public."
2.8  Configure Bucket for Static Website Hosting
In this step, you will configure your S3 bucket to host a static website.

2.9. Properties
In your bucket view, go to the "Properties" tab.

2.10. Configure Static Website Hosting
Click "Edit" in the "Static website hosting" card.
Select "Use this bucket to host a website."
Set the index document to "index.html."
Leave the error document field empty.
Click "Save changes."
Step 5: Access Your Static Website
In this step, you will obtain the URL to access your hosted static website.

2.11. Static Website Endpoint
In the "Static website hosting" card, you'll find an endpoint URL. This is where your website is hosted. It will look like http://your-bucket-name.s3-website-your-region.amazonaws.com.

2.12. Access Your Website
Open a web browser.
Enter the static website endpoint URL in the address bar and press "Enter."
Congratulations! You have successfully hosted a static website on AWS S3. Share the provided URL with others to access your website.

Troubleshooting
Issue 1: 403 Forbidden Error
If you encounter a "403 Forbidden" error, double-check that your S3 bucket and files are set to public.

Issue 2: Index Document Not Found
Ensure your index.html file is named correctly and located in the root of your bucket.

Issue 3: Website Not Updating
If changes don't reflect, clear your browser cache or ensure you uploaded the latest files to the S3 bucket.

This guide should help you host a static website on AWS S3, including where to include CSS and JavaScript scripts in the HTML file.
