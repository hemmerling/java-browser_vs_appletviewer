# java-plugin_vs_appletviewer
Browser vs. Appletviewer - Test of the "codebase" and "archive" parameters of a Java applet

By this project, I explore how to call a Java applet by a HTML page, by both a browser and the Java appletviewer.

* Java 8, on Windows.
* Firefox browser.

## Appletviewer doesn't like a relative path with the "archive" parameter ##

"jrun1.bat",
"jrun2.bat",
"jrun3.bat",
"jrun5.bat"
run properly.

jrun4.bat
loads the HTML file "4_fails_with_appletviewer.html" and aborts operation with

    java.security.AccessControlException: access denied ("java.io.FilePermission"   
    "\C:\Users\Public\archive\github\java_browser_vs_appletviewer\applet_awt.jar" "read")

So the appletviewer doesn´t like a relative path with the "archive" parameter, e.g. 'archive="../applet_awt.jar"'

## The Java plugin for browsers don't like a relative path with the "codebase" parameter ##

"3_works_with_browser_and_appletviewer.html",
"4_fails_with_appletviewer.html"

may be properly loaded by a browser.

Firefox browser fails to load the Java applet by the HTML file "5_fails_with_browser.html".

So browsers don´t like a relative path with the "codebase" parameter, e.g. 'codebase="../"'



