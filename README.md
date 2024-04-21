# PokeMatch: A Simple DevContainer Project

## Project Overview

- We are building a straightforward web     application that connects to a MongoDB database.
- The frontend is coded in HTML, CSS, and JavaScript.
- Similarly, the backend is implemented in JavaScript       using      Node.js.
- Within the web app, users can play a memory game, and their   moves/time to finish the game are saved.
- There's a leaderboard showcasing the top 5 players.
- The leaderboard ranks players based on the number of moves required to complete the game.

## DevContainer Setup


<a href="https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/lorenzboss/pokematch.git">
  <img 
    src="https://img.shields.io/badge/Open_in-DevContainer-blue?logo=visual-studio-code" 
    alt="Open in DevContainer" 
    height="30"
  >
</a>

### Starting the Project via Button

1. Ensure you have installed [Docker](https://www.docker.com/get-started) and [Visual Studio Code](https://code.visualstudio.com/download) with the [DevContainer](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension
2. Click on the button above (on [github](https://github.com/leandroaebi/pokematch))
3. All dependencies, extensions and tools will be installed automatically
4. Duplicate the `.env.sample` file and rename it to `.env`
5. Launch the project with `F5` or `Ctrl+F5` or `npm run dev`

### Starting the project manually

1. Ensure you've installed [Docker](https://www.docker.com/get-started) and [Visual Studio Code](https://code.visualstudio.com/download) with the [DevContainer](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension
2. Clone the repository in Visual Studio Code
3. Reopen the project in a DevContainer
4. All necessary dependencies, extensions, and tools will be automatically installed.
5. Copy the `.env.sample` file and rename it to `.env`
6. You can Run the project with `F5` or `Ctrl+F5` or `npm run dev`

### Initialize sample data

To add sample data to the database, execute the following command in the terminal (within the pokematch folder):

```bash
node sample-data.js
```

### Additional information

1. The website will run on port `4040`
2. The database tool, mongo-express, will be accessible via port `8081`
3. Credentials for mongo-express are `admin` and `pass`
4. The database is running on port `27017` (direct access is unnecessary)

### Tools

Within the DevContainer, you can utilize the following tools and extensions:

- Mongo-express
- ESLint
- Prettier
- REST Client

## Production container

### Starting the project

1. Confirm that you've installed [Docker](https://www.docker.com/get-started)
2. Clone the repository
3. Navigate to the repository folder and execute the following commands:
4. In the terminal, navigate to the pokematch folder and execute the following commands:
   ```bash
   docker build -t pokematch_production .
   ```
   ```bash
    docker run -d -p 4040:80 --name pokematch_production pokematch_production
   ```

### Additional information
1. The project will operate on port `4040`
2. As the database is not included in the production container, the leaderboard functionality will be disabled.










