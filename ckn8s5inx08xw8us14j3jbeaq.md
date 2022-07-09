## ⚡ TIL: Creating your own npm package

#### First of all, **What is npm?**

**npm** is two things: first and foremost, it is an online repository for the publishing of open-source Node.js projects; second, it is a command-line utility for interacting with a said repository that aids in package installation, version management, and dependency management. A plethora of Node.js libraries and applications are published on npm, and many more are added every day.

☝ This is not out of my brain. 🧠 

Reference to the definition 
 [https://nodejs.org/en/knowledge/getting-started/npm/what-is-npm/](https://nodejs.org/en/knowledge/getting-started/npm/what-is-npm/) 

## Setting the things up

What you need to start is with simple Node.js installation and yes, that is it.
Refer to the below links 👇

[How to install Node.js](https://nodejs.dev/learn/how-to-install-nodejs)

[Download link for Node.js](https://nodejs.org/en/download/) 


## Let us break this down into simple steps


#### 1. Creating the package.json file

For publishing an npm package you don't need anything apart from package.json. But, yeah it will not be having any functionalities.

There are two ways to create the **package.json** file. You can simply open any code editor and go for the good old-fashioned way of editing it yourself. I will suggest trying it once. You will get to know how to and what to add as key-value pair in the JSON file.

```
{
    "name": "your-amazing-package",
    "version": "1.0.0",
}
```
This is the minimum key-value pair that is required to publish a package

But, again if you want things to be done efficiently. Create the package.json with the below command

```
npm init
```

![Capture.JPG](https://cdn.hashnode.com/res/hashnode/image/upload/v1617826535417/hfogJLNk8.jpeg)


Follow the instructions and enter the details one after another and after that just select enter after confirming the details.

This is how your **Package.json** is going to look after that 👇
```
{
  "name": "awesome-npm",
  "version": "1.0.0",
  "description": "the awesome package",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/YOUR_Git_USERNAME/awesome-npm.git"
  },
  "keywords": [
    "awesome"
  ],
  "author": "Sourav Dey",
  "license": "MIT",
  "bugs": {
    "url": "https://github.com/YOUR_Git_USERNAME/awesome-npm/issues"
  },
  "homepage": "https://github.com/YOUR_Git_USERNAME/awesome-npm#readme"
}
```


We have the package.json ready. Now, index.js comes to the picture that is defined in pacakge.json as "main": "index.js"


#### 2. Creating the index.js file.

Let's create a simple function in the **index.js** file. 👇

```
function awesomeEmojiLog(message) {
    if (message === undefined) throw new Error("No Message Found");
    console.log("😎", message)
};

module.exports = awesomeEmojiLog
```

It is any day better to test your function before publishing it.
It can be easily called inside index.js as 
```
awesomeEmojiLog("This is awesome emoji")
``` 
Test it with a simple command 
```
node index.js
```

The output will be 
```
😎 This is awesome emoji
```

Once done. It is now time to publish it.

#### 3. Publish the npm package

To publish an npm package you first need to create an account in the npm registry with this link 👉 [Signup for npm](https://www.npmjs.com/signup).

Done. Cool. 

Log in to npm using the terminal with any of these two commands

```
npm login
```
or 
```
npm adduser
```

Enter the **username**, **password**, and **email ID** as asked.

After that, you are one command away from your npm package. Just type this

```
npm publish
```

Note- If your package name starts with "@Your-username/packageName"

use the below command.

```
npm publish --access=public
```


🎉🥳 The npm package is Published. You will get a mail for the same and You can check your list of packages in the npm registry if you are logged in.

#### 4. Create the Github Repo for your package.

Create your repo **awesome-npm** and push the code. 

Follow the command to push the code.

```
echo "# awesome-npm" >> README.md
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/Souravdey777/awesome-npm.git
git push -u origin main
```

Add the Licence for your package. I have used MIT.

![tempsnip.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1617877466920/0-GJeGt2Q.png)

Write the package's basic details in the Readme file like how to use it and what it does. Now, you can **Create a new release** for the npm package with proper versioning.

you can check the repo for reference 👉
[https://github.com/Souravdey777/awesome-npm](https://github.com/Souravdey777/awesome-npm) 

and the npm package 👉
 [https://www.npmjs.com/package/awesome-npm](https://www.npmjs.com/package/awesome-npm) 


# 😎 
Your awesome npm package is ready. 🎉🎉

Hope you Loved it! Do let me know in the comments.

## Contact me 

- [Github](https://github.com/Souravdey777/)
- [LinkedIn](https://www.linkedin.com/in/souravdey777)
- [Twitter](https://twitter.com/Souravdey777)


