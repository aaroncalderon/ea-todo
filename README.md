# Proof of Issue

I have used a fork of the EA Todo repo to create a proof of issue for https://github.com/electron/electron/issues/6204

I modified it a little bit because I had some issues with the `live-reloead` package. In the end I removed the `live-reload` package.

So, some of the script commands on the `package.json` file are broken.

# how to use

1. Clone this repo
    ```
    git clone https://github.com/aaroncalderon/ea-todo.git -b electron-uml-issue-node-int-off --single-branch electron-uml-issue-node-int-off

    ```
    - The above command will clone only the `electron-uml-issue-node-int-off` branch for your convinience.

2. In a terminal execute the following: `cd electron-uml-issue-node-int-off && npm install`
3. and then `npm run start`

If you see any warnings about auto-updater, please disregard.

# look into the issue

I have set the todo items `task.text` to be interpreted as markdown.

If you open the developer tools you will see some errors messages. These error messages are related to showdown being loades as a `CommonJS/nodeJS` module, instead of as a `Regular Browser` (no loading) behaviour. 

# difference from electron-uml-issue

I have set the `nodeIntegration: flase` property of the created BrowserWindow and behaviour is as expected. 

# EA Todo

Application for introduction series on integrating AngularJS with Electron. Introduction series can be found [here](http://electron.rocks/electron-angularjs/).

![image](preview.png)


