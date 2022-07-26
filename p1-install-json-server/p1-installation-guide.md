## Install `json-server`

To create RESTful web service in no time, you can use `json-server`.

It is a Node package.

Node provides runtime environment for executing JavaScript code on server side.

Installing `Node.js` installs `node package manager` - `npm` tool that helps in installing and managing Node packages.

With `json-server`, on the local machine, the web service can be started with a .json file containing the data that needs to be served.

It helps to simulate server and create client-side application using the fake APIs.

### Installation Steps

1. Install `Node.js` (if not already installed)

    - Download the installer code from [here](https://nodejs.org/en/download/)
    - The page provides installer options for all 3 popular operating systems: Windows, Mac and Linux

2. Installation of `Node.js` also installs `npm` tool

3. Confirm the version and installation of `Node.js` and `npm` by running commands on command terminal:
    - `node --version`
    - `npm --version`

4. Install `json-server`
    - To install `json-server`, From the command terminal, run the command `npm install json-server -g` 
    - The `-g` option allows installing `json-server` at the global level. 
    - This will allow `json-server` to be started from any folder in the system.

5. Confirm the version of `json-server` installed, using the command 
    - `json-server --version`

5. Start `json-server`
    - To start `json-server` on default port for the data residing in `db.json` file, run the command `json-server db.json`
        - If no port is specified, by default the server runs on port `3000`.
        - If the file `db.json` file does not exist, the server creates a `db.json` file with sample data for `posts`, `comments`, and `profile`
        - The successful start up of server shows the following output
        ```
            \{^_^}/ hi!

            Loading db.json
            Oops, db.json doesn't seem to exist
            Creating db.json with some default data

            Done

            Resources
            http://localhost:3000/posts
            http://localhost:3000/comments
            http://localhost:3000/profile

            Home
            http://localhost:3000

            Type s + enter at any time to create a snapshot of the database
        ```
        - If the file exists, the server starts and with the data available
        - Ensure `json` data is correctly defined in the `.json` file.
    - To start `json-server` on a different port, use the `-p` or `--port` option followed by port number on which the server should run.
    - The command `json-server -p 3001 db.json` starts the `json-server` on port `3001`
    - This option is useful when multiple services need to be started through `json-server`, and run simultaneously. Each service can be allocated a different port number while starting `json-server`
    - For more help on `json-server`, run the command `json-server -h` or `json-server --help`.


