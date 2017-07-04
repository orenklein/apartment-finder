# apartment-finder


## Usage
* Create a config.json and put it in the root folder
```
{
  "dispatcher": {
    "type": "email",
    "email": {
      "from": "your-replyto-address",
      "to": ["your-email-address"],
      "sendgridApiKey": "your-sendgrid-api-key"
    }
  }
}

OR

{
  "dispatcher": {
    "type": "github",
    "github": {
      "authentication": {
        // Any of the options in https://github.com/mikedeboer/node-github#authentication
      }
      "repoOwner": "github-username",
      "repoName": "repo-name",
      "labels": ["labels to label your new issues with", "can be a few labels"]
    }
  }
}

```

* Edit query.js
* Install dependencies:
```
npm install
```
* (windows users - first install curl https://curl.haxx.se/download.html and java jdk http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
* Download and install selenium standalone server:
```
curl -O http://selenium-release.storage.googleapis.com/2.53/selenium-server-standalone-2.53.1.jar
```
* Download the Chrome WebDriver from: https://sites.google.com/a/chromium.org/chromedriver/downloads
* Start selenium standalone server with Chrome webdriver:
```
java -jar -Dwebdriver.chrome.driver=$(pwd)/chromedriver selenium-server-standalone-2.53.1.jar
```
* Run
```
node index.js
```
