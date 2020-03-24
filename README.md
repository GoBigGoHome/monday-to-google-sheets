# monday-to-google-sheets
Pulling Monday.com data into a Google Sheet
I am not an expert but I finally found a way that sort of works for us. I was equally getting frustrated that Zapier's ability to push Monday data efficiently to Sheets was not there. More so the other way around but there was another post here about that and I was able to get Sheets to speak to Monday in a blast vs one column change at a time through Zapier. 

The challenge with my solution is that it does not trigger from Monday. I have mine triggering once a day over night. What I have attached is a sample of my code that I have in my script editor in my Google sheets set on a time based trigger. I have three functions. 

Function 1 is the API call. This will be the function that reaches out to Monday and gets the information back to sheets. 

Function 2 gets all my boards and their ids from my Monday account and puts them into a sheet. It sets up the query details and tells function 1 what the call for then parses the data into the columns in my sheet. 

Function 3 is a little more advanced. It gets all items (or pulses) from my Monday account and puts them into a sheet. It sets the query, sends to function 1 for the call and then parses the data and nested object to put the item name, item id, the board name, and board id from that item. 

From these you can do a lot more. Hypothetically you could create a complete mirror of your entire Monday account by using multiple functions where you search your boards and get their ids and column names. Then for each board create a sheet with the necessary column headers. Then for each board call all the items, their ids, and their column values, and fill them into the sheets. 

Hope this helps! If you need support feel free to reach out. I am not an expert and this is my first time every posting on a forum...
