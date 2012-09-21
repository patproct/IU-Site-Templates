INDIANA UNIVERSITY BRANDING BAR AND FOOTER

Overview and Instructions

----------------------------------------------------------------------------
For more information, see http://visualidentity.iu.edu/media/downloads.shtml
----------------------------------------------------------------------------

This branding bar and footer kit has been created to enable anyone within Indiana University to build Web sites that conform to Indiana University's visual identity guidelines. The instructions below and inline documentation (HTML and CSS comments) are written so that Webmasters with a basic understanding of HTML and CSS can quickly and easily implement the branding bar and footer on their Web sites.

----------------------------------------------------------------------------
Web Standards
----------------------------------------------------------------------------

The files included in this kit have been programmed using valid, semantic XHTML 1.0 Transitional markup for structure and valid CSS for presentation. They have been tested on all of the following browsers:

Windows:
	
    	* Firefox
    	* Internet Explorer 6 - 7
    	* Safari

Macintosh:

    	* Firefox
    	* Opera
    	* Safari

The XHTML and CSS are valid according to the W3C's HTML [http://validator.w3.org/] and CSS [http://jigsaw.w3.org/css-validator/] validators. The XHTML validates against both the Transitional and Strict doctype. 

----------------------------------------------------------------------------
Instructions
----------------------------------------------------------------------------

These instructions assume a basic knowledge of HTML and CSS. 

1. Contents
----------------------------------------------------------------------------

The branding bar kit contains the following files and folders. More information about these files and the items contained within can be found in the comments embedded in the XHTML and CSS files.

	* /css/ - Cascading style sheets

		* print.css - Print style sheet
		* screen.css - Style sheet for display on computer monitors
		* styles.css - Master style sheet import

	* /img/ - Images

		* blockiu.psd - Master Photoshop file to customize white block IU
		* blockiu_black.gif - White block IU with black background
		* blockiu_crimson.gif - White block IU with crimson background
		* blockiu_white.gif - Crimson block IU with white background (default)
		* go_red.gif - Search box "GO" button with red background (default)
		* go_white.gif - Search box "GO" button with white background
		* iub_crimson.gif - White IU signature with crimson background for crimson banner (default)
		* iub_white.gif - Multicolor (black and crimson) IU signature with white background for white banner

	* index.html - Default page with embedded branding bar and footer


2. Adding the branding bar and footer
----------------------------------------------------------------------------

First you must copy the "css" and "img" folders, along with the contents of each, to your Web account or server. If folders with these filenames already exist on your Web account or server, copy only the files within this download's "css" and "img" folders into the pre-existing folders. Be careful to not overwrite files on your Web account or server with the files from this download. If files exist on your Web account or server with identical filenames as those in this download, you will need to combine them (in the case of CSS files) or rename them and adjust all CSS or HTML files that link to those files.

The index.html file contains the structure and content of the branding bar and footer. Three blocks of code within index.html begin and end with comments that describe their contents. To add the branding bar and footer to your pages, copy the contents of each of the following comment blocks to your pages:

	* INDIANA UNIVERSITY BRANDING BAR AND FOOTER STYLES - This must appear in the <head> of your document
	
	* INDIANA UNIVERSITY BLOOMINGTON BRANDING BAR - This must be the first visible item at the top of each of your pages
	
	* INDIANA UNIVERSITY FOOTER - This must be the last visible item at the bottom of each of your pages (with the exception of background colors or images)
	
All other code in the index.html file is suggested, but not required by IU's Visual Identity program.


3. CSS options
----------------------------------------------------------------------------

Embedded in the screen.css file are the following options to alter the branding bar and/or footer. To enable any of these options, view the embedded comments at the bottom of the screen.css file.

	1. Alternate White Branding Bar
	
	Enabling this area in the CSS changes the color of the branding bar from crimson to white and the IU Bloomington signature from white to crimson.

	2. Alternate White Footer

	Enabling this area in the CSS changes the block IU and footer links from crimson to white and text from black to white.

	3. Fluid Format

	Enabling this area in the CSS changes the default page layout from 760-pixels wide and centered to left-jusitified and fluid.
	
With the exception of the font-family and background styles applied to the body tag and the width style applied to both the signature and copyright ids, no styles in the screen.css file should be altered. The font-family, background, and width styles can be altered or redefined to conform to the design of the site the branding bar and footer will be on. The font-size style applied to the body tag may be altered or redefined with the following recommendations:

	* The style uses relative or resizable units (i.e.: percents, ems, or keywords)
	
	* The footer text remains legible (i.e.: above an equivalent of 9 pixels)

	
4. Footer year stamp
----------------------------------------------------------------------------
	
By default, the year stamp embedded in the footer is static. However, the static year stamp can be replaced with scripting to enable dynamic updating, with the following recommendations: 

	* The year stamp retains its current formatting (four digits, year only)
	
	* An appropriate alternative is supplied if client side scripting is employed

Listed below are several server-side scripting options based on server or page type to create a dynamic year stamp:

	1. Using Server Side Includes (.shtml):
	NOTE: This method is recommended for those hosted on IU's central servers.
	
	<!--#config timefmt="%Y" --><!--#echo var="DATE_LOCAL" -->
	
	2. Using Active Server Pages (.asp):
	
	<% =Year(Now) %>
	
	3. Using PHP: Hypertext Preprocessor (.php):
	
	<?php print date("Y") ?>