# trello-import-apps-script
Google Apps Script to import Trello cards into a Google Spreadsheet.
Based on Robert Gebhardt script (https://stackoverflow.com/users/4847886/robert-gebhardt). 


## Prerequisites
Before installing and using the script it is necessary to:
* Get the API key and API token (https://developer.atlassian.com/cloud/trello/guides/rest-api/api-introduction/)
* Get the Trello board id (https://community.atlassian.com/t5/Trello-questions/How-to-get-Trello-Board-ID/qaq-p/1347525)

## Installing
1. Open the trello-import.gs file
2. Copy the script content
3. Open the Google spreadsheet
4. Access the menu: Tools > Script Editor 
5. Paste the script code into the newly created script file
6. Replace the content of the authentication variables:
```sh
// trello variables
var api_key = "your_api_key";
var api_token = "your_api_token";
var board_id = "your_board_id";
```
7. Save the file (Ctrl + S)
8. Enter a name for the new project, for example: "Trello import"
9. Close the spreadsheet and open it again. The onOpen() script function will be executed and after a couple seconds the Trello menu will appear as the last option on the main menu

## Running
1. Access the menu: Trello > Update from Trello
2. A dialog will appear informing you of the available lists. Choose one of the lists by filling the list name, or leave it blank to import all lists
3. The script will add lines to the end of the spreadsheet with the content:
```sh
[Member_Name, Card_Name, Creation_Date, Due_Date, null, Card_Description, List_Name]
```
