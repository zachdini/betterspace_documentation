# Betterspace Documentation
This is the full documentation of the BetterSpace platform. This document is written for developers, data scientists and any stakeholders that want to understand the development principles behind the BetterSpace platform.

## Intro

Approximately 1 in 4 people in the UK will experience a mental health problem each year. BetterSpace is building a wellbeing recommendation algorithm to help people find what is most likely to help their mental health. It’s a big project, and we’re developing the key areas of the functionality through a series of pilots with several companies over the next 6 months. The pilot will test the basic functionality, from data capture to the solutions we include, and inform our future technical development and customer experience. 

## What is BetterSpace

BetterSpace is a workplace mental health service developed as a web based platform. The backend is hosted on a serverless architecture in AWS. The front end is a ReactJS single page webapp.

## Repo guidelines
- Tasks will be agreed at the beginning of coding week, the product owner (Alfredo) will decide which tasks have priority and define a list of subtasks using Wrike (https://www.wrike.com/workspace.htm)

- Developers should also create subtasks with completion time to track progress. Ideally each subtask falls into a 2, 4 or maximum 8 hours length.

- The code repository lives at Github (https://github.com/Belfio/betterspace_testing)

- The developers will have to provide a user name to alfredo@betterspace.uk in order to gain access and to be able to fork the project.

- Developers will develop features and regularly generate Pull Requests (PR) to the master branch of the project. Branches will be labeled as: Developer/Feature

- Code is expected to be committed with proper title and description, and signed by the developer (git commit -s) with Linux Kernel style. Please follow the format already on the repository with
[SECTION] Title (issue number if any) Sensible description of changes Signed-off-by: developer@domain.com

- Developers are expected to rebase their changes at least twice per week to avoid spending too much time resolving merge conflicts.

- Only PR features in a working state, rebase and test before commit. Don’t break others people builds.

- The maintainer (Alfredo) will validate the feature and let the code merge into the master branch after being agreed.

- A demo will occur at the end of the week on Fridays to sync into the progress and decide the new steps.
