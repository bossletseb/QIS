# QIS grade checking tool
Checks for students at FH Aachen whether a new exam grade has been uploaded to the grade portal [QIS](https://www.qis.fh-aachen.de/qisserver/rds?state=user&type=0) and subsequently notifies them with their result

## Before using the tool
- Clone repository or download as ZIP, keeping all files in the same folder
- Download [geckodriver](https://github.com/mozilla/geckodriver/releases/tag/v0.30.0) and place in the same folder you just cloned/downloaded
- [Mozilla Firefox](https://www.mozilla.org/en-US/firefox/browsers/) and [Java Runtime Environment 1.8](https://www.java.com/en/download/manual.jsp) must be installed

## How to use
- Open 'Configurator.jar'
- Stay on 'General' tab and input credentials you use to log into [QIS](https://www.qis.fh-aachen.de/qisserver/rds?state=user&type=0)
- Press 'Test QIS' button to verify QIS credentials have been entered correctly
- Select Notifications option in dropdown
- If Telegram: input Telegram API Token and Chat ID (see Notifications section on how to get credentials)
- If G-Mail: input G-Mail address and password (see Notifications section for further instructions) 
- Press 'Test Notification' button to verify credentials (expected outcome: "Connection successful" message received on selected notification platform)
- Change to 'Modules' Tab
- Use 'Fetch All' button to add currently exams you are currently registered for
- Add additional modules as required (by module ID as found on QIS)
- Press 'Run QIS' button for one-off validation or;
- Set up task scheduler routine for regular validation -> use 'QIS.jar' as application to run

## Notifications
- Telegram: [Follow step 1 to 3 on how to set up your own bot](https://sendpulse.com/knowledge-base/chatbot/create-telegram-chatbot) which will send you notifications, as well as [how to obtain the chat id](https://www.alphr.com/find-chat-id-telegram/#:~:text=still%20pretty%20nifty%3A-,Go%20to%20https%3A%2F%2Fweb.telegram.org.,are%20actually%20your%20chat%20ID) of your own bot 
- G-Mail: Instructions on [account settings required](https://support.google.com/a/answer/6260879?hl=en) to allow notifications 

### Current version is set up for students studying "Angewandte Mathematik und Informatik" (AMI) in Cologne. 
- For all other degree programmes, add module id and name to modules.json, using the same format of the file provided.
- If you are studying AMI but in Juelich (1) or Aachen (0), replace the fifth digit of each module with the number shown in the bracket.
