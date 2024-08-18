# Procore Integration Project

## Overview

This project integrates with Procore's API, allowing users to log in using their Procore accounts, view projects, and access project worker information. The application supports OAuth authentication and includes features to fetch and display project and worker data.

## Features

- **OAuth Authentication:** Users can log in with their Procore accounts using OAuth.
- **Project Listing:** View a list of projects available to the user.
- **Project Worker Details:** Retrieve and display information about project workers.
- **Error Handling:** Displays messages when no projects or workers are available.
- **Dynamic Data Handling:** Uses AJAX for fetching data and updating the UI without reloading the page.

## Setup

### Prerequisites

- **Java 21** (or compatible JDK version)
- **Spring Boot 3.1.4** or higher
- **PostgreSQL** database
- **Procore API Access** with OAuth credentials

### Environment Configuration

Update the `application.properties` file with your Procore OAuth credentials and production URL:

```properties
# OAuth Configuration
oauth.client-id=YOURCLIENTID
oauth.client-secret=YOURCLIENTSECRET
oauth.redirect-uri=http://localhost:3000/callback
oauth.token-url=https://login.procore.com/oauth/token
oauth.authorize-url=https://login.procore.com/oauth/authorize
