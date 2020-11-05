# Sessions Rating Screen

* Duplicate one of the previous screens
* rename the screen to "SessionsRating"
* Delete the Gallery
* change the .text property of the Title label to "Session Rating
* disable the sessions rating icon in navigation
* enable the twitter icon in navigation
* set the .onSelect property of the twitter icon to `navigate(twitter)
* go to your other screens and set the .onSelect property of the sessions rating icon to `navigate(SessionsRating)`
* click on `data`
* Connect your app to your new CDS entity
* Create a form --> Edit
* Set the .DataSource property of the form to the name of your CDS Entity
* Click `Edit fields` 
* Remove the `Created at` field
* Add all fields that you created in the previous step. 
* Change the session name field to a dropdown
  * click `edit fields`
  * Select `Allowed Values` in `Content Type`
* Make the dropdown show the session name 
  * Select the SessionName DataCard, change allowed values to `Office365Outlook.CalendarGetItems(Dropdown1.Selected.Name).value`
  (if you want, you can Sort() by Start
  * Change the Data Value of your Dropdown to `Subject` (its `Body preview` by default, which would be the session description)
  * Change the .Update property to DataCard.ValueSubject (as we want to display the subjects of our events here)
* Work on the fields - we want pretty rating stars *****
  * Change Content Type of all other fields to `Edit Rating`
  * in case you dont have a pretty display name, you may now change the display name of your fields
  
* Create a icon for "submit"
* Create an icon for "cancel" 
* position them in the top right and left corner

You can now proceed to the next step: [Success Screen](https://github.com/LuiseFreese/M365BootCamp/blob/main/MakeYourApp-SuccessScreen.md)
