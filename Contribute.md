## Installation Steps
 - Install node js locally
 - Clone the repo
 - Install dependicies(npm install)
 - Start the DB locally
   - docker run -r POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres
   -Go to neon.tech and get yourself a new db
- Change the .env files
- npx prisma migrate
- npx prisma generate
- npm run build
- npm run start


## Docker installation
- Install docker 
-Create network
  - docker create network my_network
- Start postgres 
   - docker run --network my_network -e POSTGRES_PASSWORD=mysecretpassword --name postgres -d -p 5432:5432 postgres
- Build the image 
   - docker build -t --network=host user_project .
- Start the image
   - docker run -e DATABASE_URL=postgresql://postgres:mysecretpassword@postgres:5432/postgres --network my_network -p 3000:3000 user_project


## Docker compose 
-Install docker,docker-compose
-Run  `docker-compose up`
 

