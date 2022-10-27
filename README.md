# CMPG-323-Project-4---24361879
RPA and Testting

WElcome to my Project 4 REadMe file.
The project started off with a bunch of training courses that prepared me for my work using automation and uipath.
I learnt about asset management in orchestrator.
I learnt how to publish from uipath studio into the cloud where my orchestrator is situated.

I have commited 6 times to github and published 5 times to my personal workspace in orchestrator.
THe project starts off by automating the username and password of a user whose login credentials are stored in assets.

uipath studio uses a secure string value to store the password and send the bLoginSuccess variable to be passed.

Login is successfull and you'll access the home page of the project. 

No work will need to be done and the zone page will start working. Zones data read from the provided csv will populate their relevant fields on the
webpage. It is able to do this because of an excel process I used. the process gets the range of the sheet it's working with and reads all the data within the range
to the relevant data tables in uipath. In my project the zone sheet in excel is read to the data table dtZone in uipath studio.

I then used a for each workflow to iterate through the rows of the zones sheet. It'll do this for my category sheet as well as my device sheet. 
Inside the for each i placed a navigate browser activity to open the relavant webpage and then I followed this up with a type into activity to enter the row data.
In order to distinguish between columns in a row a used a get activity to get the neccessary columns out of the csv file. I used the real column names in a string and
assigned a string variable to each column e.g "ZoneName" is represented by variable = zoneName.

AFter the webpag fields have been populated I click the create button and subsequently the record is created.

The process is the same for category sheet and in most part for the device sheet.
The only difference on the device data table is that it contains information from the previous two data tables i.e. dtZone and dtCategory.
When a the device data table is iterated over the zone and categroy data tables neeed to have been created in order for their data fields to show 
on the devices webpage.

Furthermore, Device has a check box which signifies whether or not the device is active and this box is checked on some data and not on others.
I used an "if then else" statement to check all instances that represent as TRUE in the csv file for that coloumn of data and unchecked for FALSE.

After each iteration of the device process i return back to the list so that when the process is done running that the user can view all the created devices items.
I then implement testing on two records i.e. D03 and D04 to test results. I then use a write cell activity inside the excel process to change the values of the cell to
TRUE if the process was created successfully and FALSE otherwise.

If you want to see it in action all you have to do is delete all the current entires on the website and then click run and the whole process will be run from
login to test results.

THis conlcudes my Project 4.

Below is a screenshot of my process in orchestrator.

![Screenshot (17)](https://user-images.githubusercontent.com/66521420/198247156-ad9e6953-b755-412f-ab46-284741635b28.png)
