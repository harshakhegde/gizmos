# gizmos
Scripts to ease your daily work


## Open page

This script throws a pop up where you can enter the search field for a given site
- For example, for Linked in keying in jobs, opens the LinkedIn jobs page, keying in feed opens your feed
- Create any bookmark, edit the Url to this below script

```
javascript:(function() { var targetUrl = "https://www.linkedin.com/"; new Promise ( (setQuery) => {var input = window.prompt("GoTo?:"); if (input) setQuery(input);} ) .then ( (query) => window.open(targetUrl + query) ); })();
```
You can change the base Url to any other site that you open often, like your Jira page and all you have is the Jira number :)


## Wi-Fi toggle
On Mac, If you have many Wifi networks and you want to specifically connect to a SSID, then this is your command line option

```
networksetup -setairportnetwork en0 NameOfYouWiFi PasswordOfTheWifi"
```
Note in my computer the Wi-Fi interface is **en0**, to know yours run the below command note the interface

```
networksetup -listnetworkserviceorder
```

## Bulk Accept LinkedIn requests
```
var x = document.querySelectorAll('button.artdeco-button--secondary')
for (var i = 0; i < x.length; i++) {
  setTimeout(function(idx) {
    if (x[idx]) {
      x[idx].click();
    }
  }, 1000 * i, i);
};

```

## Cowsat Darth Vader
Copy the cow file into /opt/homebrew/Cellar/cowsay/<version>/share/cowsay/cows