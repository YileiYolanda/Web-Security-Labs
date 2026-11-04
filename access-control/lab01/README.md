# Insecure direct object references

## Description
This lab stores user chat logs directly on the server's file system, and retrieves them using static URLs.

Solve the lab by finding the password for the user carlos, and logging into their account.

## Solution
1. Select the Live chat tab.
2. Send a message and then select View transcript.
3. Review the URL and observe that the transcripts are text files assigned a filename containing an **incrementing number**.
![Picture](lab01-01.png)
4. Change the filename to `1.txt` and review the text. Notice a **password** within the chat transcript.
![Picture](lab01-02.png)
5. Return to the main lab page and log in using the stolen credentials.

## Question


## Conclusion