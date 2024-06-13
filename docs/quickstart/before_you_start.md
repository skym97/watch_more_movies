---
layout: page
---

# Before you  start a tutorial

These are the steps you must do before you can run
the tutorials for the **Watch More Movies service**.

Expect this preparation to take about 20 minutes to complete.

## Preparing for the tutorials

The following instructions describe how to prepare for running the tutorials on Windows.
For information about how to prepare MacOS for the tutorials, visit the [MacOS installation guide](quickstart/macos_installation.md).

### To complete the tutorials in this section, you need the following:

* A [GitHub account](https://github.com)
* A development system (PC, Mac, or Linux) running a current or
long-term support (LTS version of the operating system).
* The following software on your development system:
    * [Git](https://docs.github.com/en/get-started/quickstart/set-up-git) (for the command line)
    * [GitHub Desktop](https://desktop.github.com) (optional)
    * A fork of the [Watch More Movies repo](https://github.com/skym97/watch_more_movies)
    * A current/LTS version of [node.js](https://nodejs.org/en/)
    * A current version of [json-server](https://www.npmjs.com/package/json-server)
    * A current copy of the database file. You can get this by syncing your fork.
    * **TIP**: If you're using a fork of the repo, create a working branch in which to do your tutorials. Create a new branch for each tutorial to prevent a mistake in one from affecting your work in another.
    * The [Postman desktop app](https://www.postman.com/downloads/). Because you run the **Watch More Movies service** on your development system with an `http://localhost` hostname, the web-version of Postman can't perform the exercises.

## Test your development system

To test your development system, follow these steps:

1. Create and checkout a test branch of your fork of the To-Do-service repo. Your `GitHub repo workspace` is the directory that contains your fork of the `Watch More Movies` repo.

    ```shell
    cd <your GitHub repo workspace>
    ls
    # (see the watch_more_movies directory in the list)
    cd to-do-service
    git checkout -b tutorial-test
    cd api
    json-server -w watch-more-db-source.json
    ```

    If your development system is installed correctly, you should see
    the service start and display the URL of the service: `http://localhost:3000`.

2. Make a test call to the service.

    ```shell
    curl http://localhost:3000/movies
    ```

3. If the service is running correctly, you should see a list of users from the service, such as in this example.

    ```js
    [
    {
      "movie_name": "Pulp Fiction",
      "genre": "thriller",
      "year": 1999,
      "country": "USA",
      "language": "English",
      "id": 2
    },
    {
      "movie_name": "How to Train Your Dragon",
      "genre": "animation",
      "year": 2010,
      "country": "USA",
      "language": "English",
      "id": 3
    }
    ]
    ```

If you don't see the list of movies, or receive an error in any step
of the procedure, investigate and correct the error before continuing.
Some common situations that cause errors include:

1. You mistyped a command.
2. You aren't in the correct directory.
3. A required software component didn't install correctly.
4. A required software component isn't up to date.

If you see the list of movies from the service, you're ready to do
the tutorials.
