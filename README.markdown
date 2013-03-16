# firefoxhtmltopdf

### DESCRIPTION

firefoxhtmltopdf will create a PDF from an HTML document (or other URL) on Mac OS using Firefox.

It uses a bit of Perl and a bit of AppleScript to get the job done. This means it needs to be run interactively, but it
will handle all of the dialogs for you.

Usually you would want to use wkhtmltopdf for something like this, but, unfortunately, page-breaking is broken in WebKit.
This means that sometimes elements can be split across two separate pages (like a &lt;tr&gt;).

Firefox (Gecko), on the other hand, seems to handle page-breaking fairly well.

### USAGE

    # A local file:
    firefoxhtmltopdf input.html output.pdf

    # A remote URL:
    # (The "6" is a delay factor to delay the print process until
    # the page has had a chance to load)
    firefoxhtmltopdf http://example.com output.pdf 6 

### AUTHOR

    Robert Krimen <robertkrimen@gmail.com>
