PURPOSE
This app allows a user to query the weather in any city across the world via the OpenWeatherMap API. Search by city, zip code, and country to view the coordinates, temperature, and current weather conditions in that location.

Note on how to use the search function of this application: This application utilizes the OpenWeatherMap API for weather queries. OpenWeatherMap does not allow search parameters that involve state names as search terms. You can search based on city or zip. You can also search for a specific city/country combination by searching "city,country_code" or "zip,country_code", where country_code is the two character representation of the country name.
Search examples: "12601", "Poughkeepsie", "12601,US"

View the app: My version of the app is viewable at the following locations.

https://venuto-weather.herokuapp.com
whatstheweather.us-east-1.elasticbeanstalk.com
HOW TO RUN
This app runs via a container that you can push to your DockerHub Account. To get started, clone this git repo to your local machine and cd into the marist-mscs621-2019-evenuto directory. You will also want to make sure you have Docker installed on your desktop. Once in the working directory, execute the following command:

 docker build -t <YOUR_DOCKERHUB_ID>/whatstheweather .
This command builds your container. Make sure to substitute your personal DockerHub account ID into the command. Next, get your image up and running by executing the following command:

 docker run -p 8888:5000 <YOUR_DOCKERHUB_ID>/whatstheweather
This command uses port 5000 for the server inside the container and exposes the application externally on port 8888. In your browser, open up localhost:8888, and you should be able to view the running application!

CLOUD DEPLOYMENT
Once you have pushed your docker image to DockerHub and have verified that it is running as expected, you can connect the app to cloud providers such as AWS and Heroku.

Cloud architecture diagram - This diagram shows the local cloud development, cloud deployment, and communication between these services and the OpenWeatherMap API.
