# Betterspace Documentation
This is the full documentation of the BetterSpace platform. This document is written for developers, data scientists and any stakeholders that want to understand the development principles behind the BetterSpace platform.

## Table of contents

1. [Intro and mission](#intro-and-mission) 
1. [What is BetterSpace](#what-is-betterspace) 
1. [Repo guidelines](#repo-guidelines) 
1. [User journey](#user-journey) 
1. [Front end](#front-end) 
1. [API](#api) 
1. [Back end](#back-end) 
1. [Data](#data) 



## Intro and mission

Approximately 1 in 4 people in the UK will experience a mental health problem each year. BetterSpace is building a wellbeing recommendation algorithm to help people find what is most likely to help their mental health. It’s a big project, and we’re developing the key areas of the functionality through a series of pilots with several companies over the next 6 months. The pilot will test the basic functionality, from data capture to the resources we include, and inform our future technical development and customer experience. 

## What is BetterSpace

BetterSpace is a workplace mental health service developed as a web based platform. The backend is hosted on a serverless architecture in AWS. The front end is a ReactJS single page webapp.

## Repo guidelines
This documentation is written for developers, data scientists and any stakeholder, wanting to understand in detail how the platform works.

The developers working in any of the BetterSpace repos, are asked to agree to the following points:
- Write your code with love and passion, someone (Alfredo ?), will read it.

- Tasks will be agreed all together at the beginning of the coding week, the product owner (Alfredo) will decide which tasks have priority and define a list of subtasks using Wrike (https://www.wrike.com/workspace.htm)

- Developers, please (!), also create subtasks with completion time to track progress. Ideally each subtask falls into a 2, 4 or maximum 8 hours length.

- The code repository lives at Github (https://github.com/Belfio/betterspace_testing)

- The developers will have to provide a user name to alfredo@betterspace.uk in order to gain access and to be able to fork the project.

- Developers will develop features and regularly generate Pull Requests (PR) to the master branch of the project. Branches will be labeled as: Developer/Feature

- Code is expected to be committed with proper title and description, and signed by the developer (git commit -s) with Linux Kernel style. Please follow the format already on the repository with  
`[SECTION] Title (issue number if any) Sensible description of changes`  
Signed-off-by: developer@domain.com

- Developers are expected to rebase their changes at least twice per week to avoid spending too much time resolving merge conflicts.

- Only PR features in a working state, rebase and test before commit. Don’t break others people builds.

- The maintainer (Alfredo) will validate the feature and let the code merge into the master branch after being agreed.

- A demo will occur at the end of the week on Fridays to sync into the progress and decide the new steps.

**[🔝 back to top](#table-of-contents)**

## User Journey
This section describes very briefly the journey that brings a company and its employees to start using our platform. Developers should derive from here the relationship among all the stakeholders, and what drives them using and promoting BetterSpace.

### Step 1: The sale
Employers that express interest in BetterSpace usually fall in one of these two categories:
- extremely progressive employers that have always sought the best solutions for their employees, or
- extremely bad employers that have never cared about company culture and are now paying the debt on GlassDoor

In both cases they are looking for the best solution to their employees' wellbeing. 
Something that brings: 
- improved employee wellbeing
- high morale for internal culture
- something great to tell new recruits

Once the employers agree to purchase the BetterSpace service, they will take part in a 100 day sprint.
The employer will provide the following:
1. Number of participants and a list of emails that can sign up to the platform
1. Budget amount per participant
1. A list of resources they want to add or remove from the directory
1. The date for the kick off

### Step 2: Kickoff
A kickoff meeting takes place at the employer's office. Our team introduce the mission and the platform in front of all the employees.
The goal of this meeting is to maximize impact and engagement with the pilot.  
Once the presentation finishes, we will send an email to all the participants with instructions on how to sign up and log in. We provide the custom url usually in the format  
`company_name.betterspace.uk`.

### Step 3: Sign up
Participants sign up, receive a confirmation email and then they log in. Once logged in, they have to go through a wellbeing assessment.
This step functions as a way to:
- provide a piece of literature around mental health and the six pillars of wellbeing
- allow 10 minutes of self-reflection about their own health
- collect data on the users for the recommendation algorithm
- collect data for review of the directory creation


### Step 4: Pilot
Participants will be able to spend their personal budget, provided by their employer, on any resource we will list on the directory.
Our main goals are:
1. Improve their wellbeing
1. Leave them excited by the product
1. Leave them relying on the platform as a source of trustful resources, updated weekly
1. Let them introspect via the platform
1. Increase discussion and sharing while smashing the stigma

The activities that they can undertake on the platform include:
- Reading their wellbeing scores, compare their strongest pillars and where they may need improvement
- Accessing a set of recommendations
- Browse, discover and buy resources
- Browse and rate completed resources
- Track their wellbeing

### Step 5: Results
After completing their resources, their wellbeing scores should see an improvement. Most of their budget is usually used. We want them to have enjoyed the service and be willing to spend their own money on the platform. Therefore, we want them to:
- keep discovering new resources
- start spending their own money
- use BetterSpace as their first point of direction towards better health

**[🔝 back to top](#table-of-contents)**

## Front end
The webapp front end is at the moment the signle place used by the participants and by the admin to access the platform. It has been developed desktop-first as a few companies allowed the participants to access the platform only by the desktop.  
A thourough documentation of the front end can be found in the front end repository at: https://github.com/Belfio/betterspace_testing  

We have used **ReactJS 16.8.6** to develop the whole structure of the website.  

### Writing guidelines
The code is written on **VS Code** using the following rules:
``` javascript
{
  "eslint.enable": true,
  "python.linting.lintOnSave": true,
  "eslint.autoFixOnSave": true,
  "autoimport.semicolon": false,
  "prettier.eslintIntegration": true,
  "prettier.semi": false,
  "workbench.statusBar.visible": true,
  "editor.minimap.enabled": false,
  "editor.renderWhitespace": "all",
  "editor.renderControlCharacters": false,
  "editor.insertSpaces": true,
  "editor.detectIndentation": false,
  "editor.wordWrap": "on",
  "terminal.integrated.rendererType": "dom",
  "python.pythonPath": "/Users/alfredobelfiori/miniconda3/python.app",
  "python.linting.pylintEnabled": true,
  "workbench.colorTheme": "One Dark Pro",
  "window.zoomLevel": 0,
  "code-runner.executorMap": {
    "python": "$pythonPath -u $fullFileName"
  },
  "code-runner.showExecutionMessage": false,
  "code-runner.clearPreviousOutput": true,
  "prettier.trailingComma": "all",
  "editor.tabSize": 4
}
```


The **linting** of the code follows the AirBnB standard, with the following exceptions:
```javascript
module.exports = {
  extends: "airbnb",
  rules: {
    semi: [2, "never"],
    "no-shadow": "off",
    // Indent with 4 spaces
    "indent": ["error", 4],

    // Indent JSX with 4 spaces
    "react/jsx-indent": ["error", 4],

    // Indent props with 4 spaces
    "react/jsx-indent-props": ["error", 4],
    "ignoredNodes": [
      "JSXAttribute"
    ]
  },
}
```

### Libraries
The webapp takes advantage of a few important libraries:
- **React router 4.3.1**: it helps handling and moving through the different pages of the platform
- **Redux 6.0.0**: it helps managing storing and changing the platform data
- **Code splitter 1.2.1**: it splits the main javascript bundle  into different pieces so the brwoser loads one small package at the time
- **AWS SDK 2.382.0**: it allows the front end to communicate with the back end

### Folder organization and main architecture
The `src` folder contains the following main folders:
- `containers`: this folder contains one file per page. Each file represents one page and it contains all the business logic that gets passed to each single components. To each file it usually corresponds a folder inside the `components` folder, containing all the (usually stateless) components.
- `components`: this folder contains all the UI components and their styles. Inside, the folder `common`, contains the main library that should be used throughout the whole webapp.
- `assets`: is a folder that contains all the other files like - images, svgs, constants
- `actions`, `reducers` and `store` are three folders that contains all the relevant files to make **Redux** work.

### How to start
