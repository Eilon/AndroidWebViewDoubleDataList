Repro for HTML datalist broken in WebView
---

In Android System WebView if you have more than one `<input list='some_list'>` attached to its own `<datalist>` then only the first one works and responds to clicking/touching/typing.

It works fine in the Chrome web browser with the exact same HTML. Android System WebView from 113.0.5672.136 to 120.0.6099.43 both have the same issue.

The relevant files to the repro are:

1. File that initializes the WebView with an HTML asset: [app\src\main\java\com\example\mywebviewport\FirstFragment.java](FirstFragment.java)
1. HTML asset file with the repro HTML: [app\src\main\assets\blah.html](blah.html)

See video where the 1st dropdown works, but the 2nd one doesn't:

![](recording.gif)
