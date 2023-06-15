# flashcards-deployment

Directions and backend code to enable deployment of the flashcards app

## Overview

The flashcards app is difficult to deploy because of the way its backend is set up to also run locally. This repo will walk you through separating out your frontend code from the backend code and deploying both using Render.

## Deploying the Backend

1. Fork this repository.
2. Deploy it to Render by connecting the GitHub repo with a Web Service on Render. Change the `start` command to `npm start`.
3. Confirm that you can visit the `/decks` route on your deployment and see decks data.
4. Note the URL at which you've deployed the backend for future use.

## Setting Up the Frontend For Deployment

1. Open your existing flashcards code.
2. In `src/utils/api/index.js`, change line 5 to:

    ```js
    const API_BASE_URL = process.env.REACT_APP_API_BASE_URL || "http://localhost:8080";
    ```

3. Add, commit, and push all your changes to GitHub.
4. Deploy to Render by connecting the GitHub repo with a Static Site.
5. 