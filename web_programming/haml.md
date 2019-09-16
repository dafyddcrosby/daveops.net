# HAML
<http://haml.info>

Install
-------
	gem install haml


Syntax Cheatsheet
-----------------

	-# This is a comment line, !!! 5 does the HTML 5 doctype
	!!! 5
	%html
	  %head
	    %meta{:charset => "utf-8"}
	    %title Demo HAML page
	  %body
	    -# you can use . or # instead of %div if you're using a div tag
	    #shorthand
	    %div#content
	    = haml :footer
