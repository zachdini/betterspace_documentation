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

Approximately 1 in 4 people in the UK will experience a mental health problem each year. BetterSpace is building a wellbeing recommendation algorithm to help people find what is most likely to help their mental health. It’s a big project, and we’re developing the key areas of the functionality through a series of pilots with several companies over the next 6 months. The pilot will test the basic functionality, from data capture to the solutions we include, and inform our future technical development and customer experience. 

## What is BetterSpace

BetterSpace is a workplace mental health service developed as a web based platform. The backend is hosted on a serverless architecture in AWS. The front end is a ReactJS single page webapp.

## Repo guidelines
This documentat is written for developers, data scientists and any stakeholder, willing to understand in details how the platform works.

The developers working in any of the BetterSpace repos, are asked to agree to the following points:
- Tasks will be agreed at the beginning of coding week, the product owner (Alfredo) will decide which tasks have priority and define a list of subtasks using Wrike (https://www.wrike.com/workspace.htm)

- Developers should also create subtasks with completion time to track progress. Ideally each subtask falls into a 2, 4 or maximum 8 hours length.

- The code repository lives at Github (https://github.com/Belfio/betterspace_testing)

- The developers will have to provide a user name to alfredo@betterspace.uk in order to gain access and to be able to fork the project.

- Developers will develop features and regularly generate Pull Requests (PR) to the master branch of the project. Branches will be labeled as: Developer/Feature

- Code is expected to be committed with proper title and description, and signed by the developer (git commit -s) with Linux Kernel style. Please follow the format already on the repository with
`[SECTION] Title (issue number if any) Sensible description of changes` Signed-off-by: developer@domain.com

- Developers are expected to rebase their changes at least twice per week to avoid spending too much time resolving merge conflicts.

- Only PR features in a working state, rebase and test before commit. Don’t break others people builds.

- The maintainer (Alfredo) will validate the feature and let the code merge into the master branch after being agreed.

- A demo will occur at the end of the week on Fridays to sync into the progress and decide the new steps.

**[🔝 back to top](#table-of-contents)**

## User Journey
This section describes very briefly the journey that brings a company and its employees starting using our platform. Developers should derive from here the relationship among all the stakeholders, and what drives them using and promoting BetterSpace.

### Step 1: The sale
Employers that express interest in BetterSpace usually follow in one of these two categories:
- extremely progressive employers that have always sought the best solutions for their employees
- extremely bad employers that have never cared about company culture and are now paying the debt on GlassDoor

In both cases they are looking for the best solution to their employees wellbeing. 
Something that brings: 
- wellbeing outcome
- high morale for internal culture
- somehitng great to tell new recruits

Once the employers agrees to purchase the BetterSpace service, the employer will provide the following:
1. Number of participants and a list emails that can sign up to the platform
1. Budget amount per participant
1. A list of resources they want to add or remove from the directory
1. The date for the kick off

### Step 2: Kickoff


### Step 3: Sign up

### Step 4: Pilot

### Step 5: Results

**[🔝 back to top](#table-of-contents)**

