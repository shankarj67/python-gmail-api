python-gmail-api
================

Connect to the Gmail API using Python 3.

https://github.com/shankarj67/python-gmail-api

Only works for sending mail without an attachment, I am planning to add more capability in the future

Based on and using code from examples at: https://developers.google.com/gmail/api/


Install
-------

This is a step-by-step guide on how to get a message sender going:

1. Install requirements ($ pip3 install -r requirements.txt)
2. Go to Google APIs: https://console.developers.google.com/iam-admin/projects
3. Go Project > Create project
4. Give the project a name and wait for Google to create the project
5. From the list of APIs in the library, select 'Gmail API' and on the next screen click 'Enable'
6. On the left-hand side, click 'Credentials'
7. Click Create credentials > OAuth client ID
8. Click 'Configure consent screen'
9. Enter a Product Name and click save
10. Under 'client ID' choose other. I'm not sure what this is for, I used my project name
11. Click 'OK' to get rid of the popup
12. Click the download icon and save the file to somewhere in your project - rename it,
 e.g. 'client_secret.json'
13. Add the client_secret code to your project folder.
14. Modify the following as required: CLIENT_SECRET_FILE, CREDENTIAL_FILE, APPLICATION_NAME, MANUAL_AUTH
15. Set your sender_address which is stored in 'settings.py' file

Usage
-----



### From within your project

    Create your object using Gmail class as 
    e.g. gmail = Gmail()

    For the first time you have to run
    gmail.get_credentials() 
    
1. The first time you call the code,a new page will open for    authentication or you will be asked to go to a URL and after authenticating, copy the auth code into terminal
2. Credential file will be created in your system which will make sure that you don't have to connect everytime
    

Code example: 

Navigate to your code folder and open python shell, paste the below code line by line

    from gmail_send_mail import Gmail
    Gmail.get_credentials() 
    recipient_address = '123@gmail.com'
    subject = 'Test subject'
    body = 'Test body'
    Gmail().send_mail(recipient_address , subject, body)

Output example: 

    Sending your message, please wait...
    Message sent successfully to : 123@gmail.com

   







