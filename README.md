# Travelligence - A Travel Vacation app

### Overview
This project is travel application for people who can’t decide where to take their next vacation. 
The application prompts the user to fill out a simple sign up form and our algorithm utilizes data from the users location, estimated age, estimated culture, and a few uploaded photos to recommend a country to visit.

![Travelligence](travelligence-screenshot.gif)

### Links
- [Link to the page](https://travelligence.herokuapp.com/)
- [Link to the code](https://github.com/yuda0110/Travelligence)


### Tech/framework/API used

#### The main technologies used to narrow down travel destination for each user
- [Microsoft Computer Vision](https://docs.microsoft.com/en-us/azure/cognitive-services/computer-vision/quickstarts/javascript-analyze)

Microsoft Computer Vision analyzes the users uploaded images and extracts meta information about the image. 
We use this information to place the image into a category (outdoor_city, outdoor_scenic, food, animal, etc.) in which a group of countries will share.  
This is an important aspect of our algorithm to narrow down your place of travel.

- [Geoip-lite](https://www.npmjs.com/package/geoip-lite)

This npm package grabs the ip address from the users computer, we use this as part of our algorithm to record the users state of residence.

- [Agify.io](https://agify.io/)
- [Nationalize.io](https://nationalize.io/)
- [Genderize.io](https://genderize.io/)

These API's estimate the users age, nationality, and gender based upon their first name. 
Age is used as part of the wealth algorithm, along with your states medium income, to pair you up with a country in a similar wealth bracket. 

#### Other Tech/framework used
- JavaScript
- jQuery
- Node.js
- [express](https://www.npmjs.com/package/express)
- [express-handlebars](https://www.npmjs.com/package/express-handlebars)
- [passport](https://www.npmjs.com/package/passport)
- [morgan](https://www.npmjs.com/package/morgan)
- [nodemon](https://www.npmjs.com/package/nodemon)
- [axios](https://www.npmjs.com/package/axios)
- [sequelize](https://www.npmjs.com/package/sequelize)

### How to start the app on development
1. Go to the root directory of the app.
2. Run `npm install` in the terminal.
3. Create `.env` file in the root directory, add the following to it, replacing the values with your own once you have them:
4. Insert data to the `Countries` table in `vacation_db` by using the `db/seeds.sql`
5. Run `npm start` in the terminal.

```bazaar
### .env file

# Microsoft Computer Vision's API key and endpoint

KEY=your-key
ENDPOINT=your-endpoint

# Github's API keys

GITHUB_CLIENT_ID=your-id
GITHUB_CLIENT_SECRET=your-key

```


