# Twitter Screen

* Duplicate your sessions screen
* rename the new screen to `twitter`
* Change the Title label to "#M365Bootcamp"
* Select Data
* Connect to Twitter
* Select the Gallery
* change the Data source of the Gallery to Twitter
* set the .items property of the gallery to `Twitter.SearchTweet("#M365Bootcamp")`
* set the .text property of the Title field to `ThisItem.TweetedBy`
* set the .text property of the Subtitle field to `ThisItem.TweetText`
* change the .icon property of the arrow icon to a `#` icon
* set the .onSelect property of the `#` icon to `Launch("https://www.twitter.com/" & ThisItem.TweetedBy & "/status/" & ThisItem.TweetId)`

What we do right here is launching the specific tweet. On mobile, it will open the twitter app, if installed. On desktop, it will open a the tweet in the browser. 
`&` is used to concatenate (stich together) different strings. 
## Navigation

* disable the `twitter` icon
* enable the `sessions` icon
* set the .onSelect property of sessions icon to `Navigate(sessions)`
* set the .onSelect property of twitter icon on home screen and sessions screen to `Navigate(twitter)`

You can now proceed to the next step
