# java_browser_vs_appletviewer
Browser vs. Appletviewer - Test of the "codebase" and "archive" parameters of a Java applet

I explored how to call a Java applet by a HTML page, by both browser and the java appletviewer.

## Appletviewer doesn't like a relative path with the "archive" parameter ##
On Windows, with Firefox browser and Java 8:

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

## Browsers don't like a relative path with the "codebase" parameter ##

"3_works_with_browser_and_appletviewer.html",
"4_fails_with_appletviewer.html"

may be properly loaded by a browser.

Firefox browser fails to load the Java applet by the HTML file "5_fails_with_browser.html".


