# Y2 2019 Summer: Flask Metrics

## Setup

Before you start coding, make sure you fork and clone the repository
for this lab:
```
cd ~/Desktop
git clone https://github.com/YOUR_GITHUB_USERNAME/y2s19-flask-metrics.git
```

## Metrics Lab

Create two versions of the `logged.html` page named `loggedA.html` and `loggedB.html`. In both of them, put a form with a button, but the button should have different text for each version.

Change the `/logged-in` route in `app.py` so that it will randomly show either `loggedA.html` or `loggedB.html`.

In app.py, make two new routes: "/pressedA" and "/pressedB" and in each of them, use the function `create_metric` to record that a user has pressed a certain button.

In `loggedA.html` and `loggedB.html`, in the `<form>` tag, make the `action` parameter equal "/pressedA" or "/pressedB". This way, when the user presses the button, the POST request will be send to the function you just made that will create the metric.