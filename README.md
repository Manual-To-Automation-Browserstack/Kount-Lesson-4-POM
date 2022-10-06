![Logo](https://www.browserstack.com/images/static/header-logo.jpg)

# Manual To Automation @ Kount - Lesson 3 - Page Object Model in Playwright <a href="https://cypress.io"><img src="https://i0.wp.com/blog.knoldus.com/wp-content/uploads/2022/04/cypress.png" alt="cypress" height="22" /></a>

## Introduction

This example repository shows a good use of the Page Object Model.

---

## Installation

There are a few things that you will need before you can get started.

* NodeJS - use [this](https://phoenixnap.com/kb/install-node-js-npm-on-windows) guide for Windows and [this](https://nodesource.com/blog/installing-nodejs-tutorial-mac-os-x/) guide for Mac.
* Git for pulling down the code - follow [this]() guide for installing Git on all platforms. There are other useful guides on the website mentioned previously. Start [here](https://github.com/git-guides) anad follow through to the various links to learn more about Git. It will be very useful on your automation journey. If you have any issues with tokens or user credentials, let me know as this can trip a lot of people up.
* Visual Studio Code - You can download VS Code for free from [here](https://code.visualstudio.com/download). This is a very useful tool for writing and running your code as it has auto complete, and powerful debugging capabilities. [This](https://code.visualstudio.com/docs/introvideos/basics) is a handy starting point for how to get started with VS Code.

Once you have these installed, you are good to go to the next step.

Follow the below steps to get the code onto your local machine.

* Open a terminal. (Terminal on Mac, Command Prompt on Windows)
* Go to the directory where you want to place the code using [cd](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/cd) for Windows, and it functions mostly the same for Mac. You just use "cd" but the folder structure on Mac is different (/Users/username/Documents instead of C:/Users/username/Documents)
* Copy the following command into the terminal, (remember, you must have [Git](https://git-scm.com/downloads) installed)
```sh
git clone https://github.com/Manual-To-Automation-Browserstack/Kount-Lesson-4-POM.git.
```
* Move into the directory that you just cloned by typing
```sh
cd Kount-Lesson-4-POM
```
* When inside this directory, copy the following command and run it:
```sh
npm install
```
* Once all the dependencies are installed, you will be able to run the tests by using the following commands:
```sh
# Runs the contactus.pom.spec.js file on a single browser on BrowserStack
npm run bs-single

# Runs the login.pom.spec.js file on multiple browsers in parallel on BrowserStack.
npm run bs-parallel
```

These scripts are useful to get started. You can add more as needed in the "scripts" section of the [package.json](./package.json) file. Once you have added one, you then simply run:

```sh
npm run <insert script name>
```

# Page Object Model

The Page Object Model in [Cypress](https://www.browserstack.com/guide/cypress-page-object-model) works mostly like other Frameworks do.

It is essentially a method of reducing the amount of repeated code in your tests to increase efficiency and remove duplication. The general rule of thumb is if you have found yourself writing the same code in more than one file, then it should most likely be refactored into a page object function.

When deciding what should be a page object, it is often useful to sit down and map out what your tests do to identify repeated functionality and patterns that can be streamlined using the POM.