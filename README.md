# Liferay React Native Starter Kit

This project provides an example mobile app for utilizing Liferay's headless apis.

## Prerequisites

* This Liferay React Native App is built using [Expo](https://expo.io/) which simplifies the creation of React Native apps.
* This is a JavaScript applicaiton so you will need `node` and `npm` installed.

## Getting Started

### Building this React Native App

* ` $ npm install expo-cli --global`

* ` $ expo install`

* ` $ expo start`

## Managing the App

### Authentication

The App can be configured to use either OAuth2 or Basic Auth.

#### OAuth2

To set OAuth2 up on Liferay you will need to create a new OAuth application through Liferay's administration. Configure it as shown in the image below.

![Configuration](/dev-assets/OAuthConfiguration.png)

You will then need to enable scopes to give the OAuth application access to Liferay. I've found this to be a little finnicky and thus simply enabled everything. To test any changes you make to scopes, you will need to log out and back in on the app.

![Scopes](/dev-assets/OAuthScopes.png)

At this point it should be working.

### Permissioned Images

Viewing images that do not include guest permissions may require additional configuration in your Liferay instance. If you are using basic Auth make sure "System Settings > API Authentication > Basic Auth Header" includes your image's base url. For example: `/o/adaptive-media/*`.

### Android Emulator

In order to connect to you local Liferay instance from an Android emulator you will need to `Liferay Server URL` from the Configurations page to `http://10.0.2.2:8080`.