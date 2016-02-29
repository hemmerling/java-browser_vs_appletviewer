# java-plugin_vs_appletviewer
Browser vs. Appletviewer - Test of the "codebase" and "archive" parameters of a Java Applet

By this project, I explore how to call a Java Applet by a HTML page, by both the Java Plugin for browsers and the Java Appletviewer.

* Java 8, on Windows.
* Firefox browser.

## The Java Appletviewer doesn't like a relative path with the "archive" parameter ##

"jrun1.bat",
"jrun2.bat",
"jrun3.bat",
"jrun5.bat"
run properly.

jrun4.bat
loads the HTML file "4_fails_with_appletviewer.html" and aborts operation by the error message

    java.security.AccessControlException: access denied ("java.io.FilePermission"   
    "\C:\Users\Public\archive\github\java_browser_vs_appletviewer\applet_awt.jar" "read")

So the Java appletviewer doesn´t like a relative path with the "archive" parameter, e.g. 'archive="../applet_awt.jar"'

## The Java Plugin for browsers doesn't like a relative path with the "codebase" parameter ##

"3_works_with_browser_and_appletviewer.html",
"4_fails_with_appletviewer.html"

may be properly loaded by a browser.

Firefox browser fails to load the Java applet by the HTML file "5_fails_with_browser.html".

So the Java plugin doesn't like a relative path with the "codebase" parameter, e.g. 'codebase="../"'



