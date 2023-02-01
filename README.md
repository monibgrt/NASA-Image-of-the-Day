# Nasa Image of The Day

This application uses Nasa's APOD API to retreive an image taken on the date specified by the user. It returns the image and the explanation for the image.

**Link to project:** https://imageofdaynasa.netlify.app/

![Screen Shot 2022-09-23 at 10 25 46 AM](https://user-images.githubusercontent.com/98131320/192023782-c263c88a-7161-4b53-be44-788f8af3d885.png)

## How It's Made:

**Tech used:** HTML, CSS, JavaScript, Nasa APOD API

I created this project by generating a key on the api.nasa.gov website, I looked at the documentation that Nasa provides for the API and determined how I could pull the specific information I was looking for. Then, I took the key generated and the https request url and plugged it into Postman to verify the key worked and to get a visual on how the information in the API was structured.

Once that was complete, I started working on my code. I added an event listener to my button so when the user selected a date and hit submit that would run my function that includes a variable that contains the date the user inputs and a fetch method. The fetch responds with JSON, for the data I get back, I created a conditional, if the media type is an image it will run the 'if' statement, if the media type is a video it will then run the 'else if' statement. If the user enters a future date then the 'else' statement will run. Within the conditionals, it will set the display property to 'block' or 'none' to activate the correct media type and hide the one that should not be displayed. For the explanation, in the CSS file the element is set to 'Display: none' so in the js file, I set that to block and then from the responded JSON we set the explanation to that element.

## Optimizations

When I first wrote my code, I did not have a conditional that checked the media type so it would only return images, so when a date was selected that contained a video I would get an error code. 

## Lessons Learned:

Learned about conditionals, changing the display property with the js file.

