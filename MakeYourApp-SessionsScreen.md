# Add Sessions Screen

As we want to have a screen that displays all sessions by date, we will need to connect to our Outlook Calendar in our app. 
Click `Data`
Search `Outlook`
Connect with Office365Outlook Connector

## Title field

* Create a text label
* set its .text property to "my sessions"
* Position: x=0, Y=55
* Size: 640 x 108
* if youn like to: change color, font, fontweight

## Dropdown to chose the right calendar

Now its getting a little bit tricky. Outlook can contain several calendars, and they will all show up in our app if we don't define, which tabke we want to display. 

* Create a Dropdown Field
* set its .Items property to `(Office365Outlook.CalendarGetTables().value`

Yo can now see all your calendars in this dropdown. As we only want to show ONE specific calendar (mine is called `Events`), we will filter: 

`Filter(Office365Outlook.CalendarGetTables().value,DisplayName = "Events")`

## Gallery

As we want to display the sessions in this screen, we create a gallery

* Click `Gallery`
* Select `Vertical`
* Select `Outlook` as datasource
* Select the .items property of the gallery and put `Sort(Office365Outlook.CalendarGetItems(Dropdown1.Selected.Name).value,Start)` in it

This means, that we want to use the Office365Outlook Connector and Get Calendar Items of the calendar, that is currently selected in the dropdown field. As our dropdown field is filtered to just show the `Events` calendar, we do not need to care about it anymore. 
 
* Position:x = 0, y = 141
* Size: 640  803

In the right sidebar, 

* Layout: select `Title, subtitle, and body`
* click Fields: `Edit`
* select what you want to display- 

Some suggestions: Subject (its the title of a session), Bodypreview (its the Description of a session), StartTime. 

You may want tow work on Font color, Font weight etc. - feel free to do that!

## make your dropdown menu invisible

As our users do not need to do anything with the dropdown menu, we can't delete it (because it still contains the name of the calendar we want to use) but we can set its .visible property to `false`.

* Select dropdown menu
* Select visible
* write `false`

## Navigation

We will now copy and paste the navigation from our homescreen

* Click `homescreen`
* Select all navigation icons and labels
* copy
* click `sessions` screen
* paste
* Choose same positions as in home screen 
* enable `home` icon 
  * click `home` icon
  * set display mode to `edit`
* disable `sessions` icon
   * click `sessions` icon
   * set display mode to `edit`
   
Now we want to enable navigation between our two screens. 

* Click Home Screen
* Select `sessions` icon
* select .onSelect property
* write `navigate(Sessions)`

You will seem that IntelliSense works quite nice, automatically suggesting you, what you can put into your functions. 
 





