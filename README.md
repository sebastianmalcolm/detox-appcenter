# Detox on AppCenter React Native Demo Project

## Background

This sample project demonstrates running Detox tests prior to a regular MS [AppCenter](https://appcenter.ms/) build
* On React Native 0.56.0
* In Xcode 10.1 with Detox 9.0.4 [![Build status](https://build.appcenter.ms/v0.1/apps/b941d881-bc98-48d1-8bc6-8ddf76856b36/branches/detox_9.0.4-xcode_10.1/badge)](https://appcenter.ms)
* And using Mocha runner, currently

## Requirements

Make sure you have installed:
* Xcode (tested with Xcode 9.4.1 and Xcode 10.1)
* Node.js (`brew install node` or via nvm etc, node 8.X and up is _required_)
* react-native dependencies:
   * watchman is installed (`brew install watchman`)

### Step 1: Install Dependancies

* Run `npm install`.

## To test Release build of your app
### Step 2: Build 
* Build the demo project
 
 ```sh
 npx detox build --configuration ios.sim.release
 ```
 
### Step 3: Test 
* Run tests on the demo project
 
 ```sh
 npx detox test --configuration ios.sim.release
 ```
 This action will open a new simulator and run the tests on it.

## To test Debug build of your app
### Step 2: Build 
* Build the demo project
 
 ```sh
 npx detox build --configuration ios.sim.debug
 ```
 
### Step 3: Test 

 * start react-native packager
 
  ```sh
 npm run start
 ```
 * Run tests on the demo project
 
 ```sh
 npx detox test --configuration ios.sim.debug
 ```
 This action will open a new simulator and run the tests on it.
