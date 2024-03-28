# Docker Compose for Backend Stack

## Clone repos

```
git clone https://github.com/owenhar/P465-Tour-Management-Place-BE.git
```
```
git clone https://github.com/greeava04/P465-Tour-Management-BE.git
```

## Add config.json

In order to use this you will need to get the config.json in the teams message and copy it into P465-Tour-Management-BE/src/ so that API-Keys and other important info is present.

## Docker Compose

```
docker compose up --build
```

This command will start up all of the backend services connected to a local instance of a mongodb databse. This means no usernames, passwords, places, etc will be populated you will have to manually add them with postman or something similar. If desired I can provide scripts for doing so.

## Links in front-end

Unfortunatly I haven't had a quick way to fix this yet so any time you use a link in the front-end check where it points to. The auth service is publically hosted at my ip so you can leave that if you aren't devloping it. Otherwise all links inside `fetch` calls should be replaced with their local counterpart (ie http://localhost:3000 (for auth) or http://localhost:3001 (for place-db))