# Confluence-Doc-Simple-Version-Control
Simple version control widget for Confluence documentation. AJAX in a macro.
## But why?
Atlassian Confluence uses a Java templating engine called Velocity to build HTML pages. One of the benefits of this arrangement is easy-to-create user "macros" that are added to content pages via a WYSIWYG editor. In this case, some Js and CSS is stuffed into a macro to let users know the documentation page they are looking at might contain information from a release newer than the release they are working on. 
## How does it work?
The script makes an ajax call to a different page, which contains a hidden HTML input with the latest software version released to a production server. It parses out the major/minor/point release version, and fires a customizable warning if the page version macro contains a newer version. Macro parameters are substituted into the script where needed for version info to get passed from the UI to the script.
