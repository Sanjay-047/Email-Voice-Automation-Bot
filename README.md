# Email-Voice-Automation-Bot
Email Voice Automation Bot is an Python implementation which is Voice Automated, It converts sender's speech to text and delivered the mail to single or multiple receiver.

REQUIREMENTS:
                    
1) Language used:
•	PYTHON (3.6 or later version)
 
2) Software used:
•	PYCHARM (latest version preferred or earlier version)


3) Packages used: 

S.NO	PACKAGES NAME
1	Speech Recognition
2	Pyaudio
3	Pyttsx3
4	Pipwin
    
              

4) Operating system: 
•	Windows 7 and later versions
5) System requirements:
    Minimum Requirements:
•	Minimum 4 GB ram.
•	Minimum 500 MB disk space.

Maximum Requirements:
•	Minimum 8 GB ram.
•	Minimum 1 GB disk space.


Access needs to be given: -

Because Google does not allow external servers to send Gmail, this programme will return an authentication error. To give the server authorization to send Gmail, we must enable the option from the Gmail account settings. The steps to enable the option are as follows: -

•	Open your Gmail
•	Go to Manage your Google Account.
•	Click on the Security Scroll down a bit and click on Turn on access of Less secure app access setting.


SMTP server: -
                            Simple Mail Transfer Protocol (SMTP) is the protocol for sending email, just like HTTP is the protocol used by computers to transport web pages across the Internet. SMTP specifies how email messages should be formatted, encrypted, and transmitted between mail servers, as well as all of the various details handled by your computer after you click Send. However, because Python's smtplib module compresses these technical complexities into a few functions, you don't need to know them.


Modules being used: -

1. import smptlib: - 
                                  It's an acronym for Simple Mail Transfer Protocol, which is a protocol for transmitting and routing e-mail between mail servers. If you have a Python IDE installed on your machine, this module is already installed.


2. import speech_recognition: -
                                               It performs speech recognition both online and offline, with support for a variety of engines and APIs. To use this module, simply copy and paste the following code into a terminal or command prompt.

                                 “pip install SpeechRecognition”


3. import pyttsx3: - 
                         It's a Python-based text-to-speech conversion library that also works offline. The following is the installation syntax.

                                             “pip install pyttsx3”

4. PyAudio: - 
            By installing this module, we can easily use Python to play and record audio. The installation syntax is given: 
                           
“pip install PyAudio”


Some of them may get error while installing pyaudio, follow this:
                                       
	STEP 1: pip install pipwin
	STEP 2: pipwin install Pyaudio


5. from sys import exit: -
                          from module system, take function exit.  


6. from email.message import EmailMessage: -
                            The message submodule of email module provides us with a class named EmailMessage which can be used to represent an email message.


Objects being made: -

1. listener: -
                          The Recognizer () class of the speech recognition module's Listener object is used to recognise the user's voice input.


2. engine: -
                        This object from the pyttsx3 module's init() function is used later in the programme to convert text to speech.


Functions used in the code: -

1. def talk(text): -
                                This function takes the text as an argument and allows the system to pronounce it. After that, the runAndWait() function is called to block while all currently queued commands are processed.


2. def get_info(): -
                                The limit parameter is simply a variable that will get the value of seconds for which the mic will receive voice. If the user does not answer, the programme will be terminated via exception handling. This function will print 'Listening...' every time it is called to inform the user that the system is now listening to their response. The 'voice' variable will listen for and store anything the user says, and the 'info' variable will use Google API to record the interpreted text of the audio. Whatever is stored in the 'info' variable will be printed and then converted to small letters.


3. def send_email(receiver, subject, message): -
                                   This function will first construct an SMPT server and then manually login to it using the email address and password provided by the user. This function accepts the recipient's email address, as well as the subject and body of the text entered by the user. It will send the email to the user's email address after obtaining the relevant information.

4. email_list : - 
                     It's a list of email addresses that a user can use to send emails to several people.


5. def get_email_info(): -                   
This function will ask for the recipient's name first, then his or her email address. It will ask for confirmation after receiving the email, and if the system misinterprets the address, it will ask the user to fill it in to be secure. Following that, it will request the topic and body of the email, as well as confirmation, until the user is happy. After receiving the user's consent, the system will call the 'send_email' function, which will send the email and ask the user if he or she wishes to send.     
                             

Flow of the code: -
•	Email bot will begin by introducing himself by:
   “Hi I am E mail bot, your email assistant”
•	The function get_email_info() is called, and inside it:
1.	When input is taken, the get_info() method is called multiple times.
2.	After gathering all necessary details, the send email() function is used to send the finalised email.
