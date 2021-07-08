# Adventure Insurance

## Description

Adventure Insurance is a REST-ful service for managing your mid-quest insurance claims. Never quest without peace of mind!

## Technologies Used

- Javalin Web Framework
- Postgres SQL Database
- AWS EC2 Virtual Machine
- AWS RDS Database Management
- Jenkins CI / CD Management
- Selenium Webdriver Automation

## Features

- Client and manager account creation with secure password hashing via
  pbkdf2-hmac-sha1 algorithm.
  - Plaintext passwords are never stored!
- Clients can make new claims from a dropdown menu and add cash amounts.
- Clients can view their claims and see the approval status.
- Clients can view other plan service levels and change their current plan.
- Managers can sort existing claims by all, completed, or pending.
- Managers can accept or deny claims.

## Getting Started

- Server
  - The server can be run locally through dev.adventure.app.App, or it can be packaged into a `.jar` for distribution and deployment on remote machines. To package it, ensure you have Maven installed on your machine, and then run:
    ```
    mvn package
    ```
    in the `Server` folder (at the same level as `pom.xml`). Run the resulting `.jar` file with
    ```
    java -jar server.jar
    ```
- Client
  - The client can be similarly packaged and run using `mvn package`. If running your own server, you must insert the server url into `src/main/resources/static/settings.js`BEFORE building the `.jar`.

## Usage

- New clients and managers can be created using the appropriate buttons on the login screen.
- Clients can post new claims by selecting a claim from the dropdown, inputting an amount into the amount window, and pressing submit.
- Clients can change plans by navigating to the `Plans` page after logging in and selecting a new plan.
- Managers can change their view on the claims page with the appropriate buttons.
- Managers can approve or deny claims with the `Sí` or `No` buttons.
- Either user can log out with the `Logout` button.
