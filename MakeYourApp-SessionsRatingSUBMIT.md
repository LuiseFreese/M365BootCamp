# Make the form work

* Go to your Sessions Rating Screen
* select the `Submit` icon
* set its .onSelect property to `SubmitForm('SessionRating-form');Navigate(Success);ResetForm('SessionRating-form')`

By this, we will create a new record in our CDS entity, navigate to the success screen and reset the form. 

* select the `cancel` icon
set its .onSelect property to `Navigate(Home)` - this way we will navigate to home screen

## Notify - something went wrong

If form submission doesnt work for ANY reason, we want to give users a hint. 

* Select the form
* in the .onSuccess property, type in `Notify("Thank you for submitting your session rating",NotificationType.Success)`
* in the .onFailure property, type in `Notify("Something went wrong",NotificationType.Error)`

## Final touches

* work on navigation, you know the drill
  * enable and disable the icons
  *.onSelect property to navigate({Screenname})
  
  
## You made it! 🚀🚀🚀🚀
