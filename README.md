# M365 Token Repeater

The "M365 Token Repeater" is a tool designed for ethical hackers and security researchers. It allows users to utilize saved HAR (HTTP Archive) files from web browsers that capture the session of a logged-in user in Azure and Microsoft 365 environments.

After uploading the HAR file(s), all sessions containing Access Tokens and Refresh Tokens are displayed in a list. Users can then replay these tokens to gather information such as user lists, groups, devices, and predictions for multi-factor authentication (MFA). The collected data can also be easily exported to JSON files for further analysis.

Additionally, this tool is a standalone, client-side HTML application contained within a single HTML file. It can be downloaded and used without the need for a server or network connection, making it convenient and accessible for users. The "O365 Access Token Repeater" is inspired by Beau Bullock's GraphRunner, which can be found at https://github.com/dafthack/GraphRunner.

As a hacker and developer, I have incorporated a mix of code from GraphRunner and utilized ChatGPT to improve the HTML code, although I am not a fully professional HTML developer. 

The generated output in JSON format can also be used in my other repository to generate passwords based on the password change date, which can be found at https://github.com/quahac/Back-To-The-Last-Password (online https://quahac.github.io/Back-To-The-Last-Password/Back_to_the_last_password.html)

## How does it work

1. First, go to a web browser where a Microsoft 365 or Azure AD session is active.
2. Open the Web Developer Tools in this browser (F12 is the key shortcut).
3. Generate some traffic in the Network tab and then save this output as a HAR file. In the latest versions of Edge and Chrome, you need to enable the `Allow to generate HAR with sensitive data` option. To do this, go to `Settings (of developer tool) > Preferences > Network > "Allow to generate HAR with sensitive data"`. Once enabled, the option to `Export HAR (with sensitive data)` will appear.
4. To generate more traffic without refreshing, you could enable the `Preserve log` option in Edge and Chrome or `Persist Logs` in Firefox.
5. Save the HAR file and upload it to the **M365 Token Repeater** tool.
6. If the saved HAR file session contains access or refresh tokens, they will be available for use.



https://github.com/user-attachments/assets/8d2f2fe9-1ba9-4718-b704-9ce3d7d49a04

