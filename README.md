# friendfinder
Would you like to find a friend? Fill in this quick survey and you may be able to get that bestfriend for you!

## Usage

To use our web service, simply go to our homepage and take our survey. Immediately after submitting the survey, your perfect best friend will pop up. We also have an API you can access to the network's users and their personalized information. For research purposes.

## Technologies Used

- JavaScript
- jQuery
- node.js
- Express.js
- HTML
- Bootstrap

## Code Explanation
- Our `server.js` file sets up the Express server, specifying our port number, the npm packages that need to be loaded, and also the routes, which we have externalized
- There are 2 separate HTML files (`home.html` and `survey.html`) that serve as the front-end portion of our code; they determine what the user sees (the homepage and the survey, which will also show the resulting best match)
- Our 2 routing files (`htmlRoutes.js` and `apiRoutes.js`) determine the back-end logic (based on the request being made, the response that gets sent to the browser); the HTML routes display the survey and the homepage based on the URL that is accessed, and the API routes send back existing content in our server-side data or add new friends
- Best match is calculated by finding the friend with the minimal difference in scores and then sending that friend to the browser as a JSON object
- A modal is then toggled, displaying the the best match to the person who just took the survey
- In essense, this will also be a form of notes that you may later reference weeks later
- Friends are stored as such:

```js
{
	name: "Steph",
	photo: "https://sportshub.cbsistatic.com/i/r/2018/12/17/3d6319cc-1340-486d-bbc1-48a99b3923e7/thumbnail/1200x675/789f22e2bcf6c43e36a758763020ab39/stephen-curry.jpg",
	scores: [5, 1, 2, 3, 1, 2, 5, 1, 1, 1]
}
```