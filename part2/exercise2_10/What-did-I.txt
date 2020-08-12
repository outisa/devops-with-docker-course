To get all the buttons to work properly it was necessary to remove env variables (FRONT_URL, API_URL) from both backend and frontend Dockerfiles and build new images, which I used in docker-compose.yml -file. I added also ./database volume from previos exercise. These were the only changes I did.

I added frontend, backend and database folders in .gitignore before submitting.

