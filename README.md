WhatsApp Morning Message Automation
This Python-based project automates sending daily good morning messages via WhatsApp at a specified time each morning. Utilizing the pywhatkit library, the script integrates with WhatsApp Web to send a personalized message every day at 8 AM.

Features
Automated Messaging: Sends a predefined message to a specified contact every morning.
Customization: Easy to customize the time and message content according to personal preferences.
Reliability: Designed to run smoothly given the system meets the prerequisites like having WhatsApp Web logged in.
Prerequisites
Python 3.x
pywhatkit library
WhatsApp account
Persistent internet connection and an active browser session with WhatsApp Web.
Setup and Usage
Clone the repository:
bash
Copy code
git clone https://github.com/yourusername/whatsapp-morning-message.git
Install the required packages:
bash
Copy code
pip install -r requirements.txt
Configure your message and recipient in the script.
Schedule the script to run at your desired time using your operating system's task scheduler.
This project is a simple and effective way to keep in touch with loved ones or send automated notifications through WhatsApp. Feel free to fork, star, and contribute!




Creating the exe should be the best method. But if you want to run it with the task scheduler you can do it in this way:

Launch Window’s Task Scheduler
Look for the The Actions pane(on the right) it has the Create Basic Task action. Click on it.
This will open a wizard where you will define the name of your task, the trigger (when it runs), and the action (what program to run). Action tab is where you specify the name of your Python script to run as well as any arguments to the script.
To ensure that your Python script will run regardless of the login account that the schedule task uses, and to avoid any confusion about which version of Python is used in mixed environments (64bit or 32bit), it is recommended that you run the Python executable with the name of your Python file as an argument to the executable.

Suppose the script you want to run is C:\whatsapp.py. Instead of running the script directly, instruct the task scheduler to run python.exe with the script as an argument. For example:

C:\Python27\python.exe "C:\whatsapp.py"

The location of python.exe depends on your install. If you don’t know where it is, you can discover its location; copy and paste the following code into a new Python script then execute the script. The script will print the location of python.exe as well as other information about your Python environment.

in programs, the path to your python.exe: for instance "C:\Users\Me\AppData\Local\Programs\Python\Python36\python.exe"
in arguments, your filename with the extension: for instance "mypythonsrcipt.py"
in start in, the folder of you script : for instance "C:\Users\Me\Desktop\"


