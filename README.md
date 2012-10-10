HTML5-template
==============

This is the standard HTML5-based template for HTML24, which is to be used for every project.

To use this, simply make a clone of this GitHub Repository to the wanted folder directory of the new project.

If you choose to download this template as a ZIP-file then we advise you to remember to delete unnecessary files such as .gitignore files.

Below is a description of this HTML5 template.


CSS
---

### CSS Reset

In the beginning of the CSS-file there's a few lines of code for resetting the standard CSS. This is added to reduce browser inconsistencies in different stylings such as margins and paddings.


### Clearing floats

We've added a `.clear` and a `.clearfix` class, which are both used for fixing float problems. 

The `.clear` class is used on an empty element (fx a div-tag). This element should then be placed in the end of the element, which you want to be cleared, right before it closes. For example:

		<div class="wrapper">
		
				<h1>The .wrapper element is the element beeing cleared.</h1>
			
				<div class="clear"></div>
			
		</div>
		
The other class `.clearfix` is added as a class on the element, which you want to clear. If we use it in the same example as above:

		<div class="wrapper clearfix">
		
				<h1>The .wrapper element is the element beeing cleared.</h1>
			
		</div>


### Standard font-styles

In the CSS-file, after the two different float clearing classes, there's a list of all the header-text-tags and paragraph-tags, which has received some default values. **These should be changed to fit your current project!**


### Special Fonts (@font-face)

If you need to use a special font for your project, then use the css-way with font-face. To generate the correct css-syntax and get the correct file formats for the font-face, use a font-face generator. Use the [FontSquirrel generator](http://www.fontsquirrel.com/fontface/generator) for this. If fontsquirrel doesn't work, then use either [Code and More](http://fontface.codeandmore.com/index.php) or [Font2Web](http://www.font2web.com/).


### CSS3

Rounded corners, box shadows and other CSS3 stylings should always be discussed with the project manager for each project, before choosing a solution.

If you really want to use some CSS3, then it is advised **only** to use this to add effects, that doesn't change the layout on the page. For example you can add a [transition](http://www.w3schools.com/css3/css3_transitions.asp) effect on hover on navigation-elements. 


### Standard coding in the CSS-file

The styling in the CSS-files should be indented like in the HTML-file. This will make it easier for others to make changes in the styling if needed.


### Inline styling

Do whatever you can to avoid using inline styling as this is not semantic code. Even if you use jQuery.

If you need to add styling with jQuery, then add a class to the element instead of adding inline styling with `jQuery().css()`.


### Hover Image

When you create a button or any other element that uses a background image, which has a hover effect, then use a sprite image instead of two separate images. Two separate images will sometimes cause a delay on the hover effect (because the image isn't preloaded), that's why we use a sprite image for hover images.


Javascript
----------

We are using the javascript library jQuery as standard, and the newest will always be present in the template-files.

### Script.js

In the js-folder there is a script.js file, where all the custom jQuery code should be written. This means that javascript codes shouldn't be written in the HTML-headers, but this should be coded in separate files.


HTML
----

### Title tag

Remember to change the title tag when you begin writing your HTML for a new project.

### Favicon

For every project we will make a favicon. There is already a reference to this favicon in the head of the HTML-file.

### HTML5

As this is a HTML5 template you are allowed to use HTML5-tags. To make them recognized in old browsers (mostly Internet Explorer) we are using the javascript plugin [HTML5shiv](https://github.com/aFarkas/html5shiv). 



Optional Header References
--------------------------

There are a lot of other header references as touch icons, Google Analytics and so on, which aren't needed in all projects. Therefore we've made a list of all these optional references here, to get the right code and get it faster:

- Google Analytics (remember to change the account UA-code):

		<script type="text/javascript">

		  var _gaq = _gaq || [];
		  _gaq.push(['_setAccount', 'UA-XXXXX-X']);
		  _gaq.push(['_trackPageview']);

		  (function() {
		    var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
		    ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
		    var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
		  })();

		</script>
		
- Piwik (remember to edit the `{$PIWIK_URL}` and `{$IDSITE}`) - if you want to read more about this open source web analytics software (an alternative to Google Analytics) go to their website [here](http://piwik.org/):

		<script type="text/javascript">
			var pkBaseURL = (("https:" == document.location.protocol) ? "https://{$PIWIK_URL}/" : "http://{$PIWIK_URL}/");
			document.write(unescape("%3Cscript src='" + pkBaseURL + "piwik.js' type='text/javascript'%3E%3C/script%3E"));
		</script><script type="text/javascript">
			try {
				var piwikTracker = Piwik.getTracker(pkBaseURL + "piwik.php", {$IDSITE});
				piwikTracker.trackPageView();
				piwikTracker.enableLinkTracking();
			} catch( err ) {}
		</script>
		
- [Placeholder javascript plugin](https://github.com/danielstocks/jQuery-Placeholder) (download the file and put it in the js-folder) - This plugin adds a fallback for the HTML5 placeholder attribute in older browser, so you can use this attribute without having to think about older browsers:

		<script src="js/jquery.placeholder.min.js" type="text/javascript"></script>

- Touch icons (if you need to add a icon for Android phones, then create the icon as a ["apple-touch-icon-precomposed"](http://mathiasbynens.be/notes/touch-icons) - this removes the fancy effects on the Home Screen such as rounded corners and reflective shine):

		<link rel="apple-touch-icon" href="" /> <!-- iPhone -->
		<link rel="apple-touch-icon" sizes="72x72" href="apple-touch-icon-ipad.png" /> <!-- iPad -->
		<link rel="apple-touch-icon" sizes="114x114" href="apple-touch-icon-iphone4.png" /> <!-- high-resolution iPhone and iPod -->
		<link rel="apple-touch-icon" sizes="144x144" href="" /> <!-- high-resolution iPad -->
		
- Viewport meta tag - This should be used if you style your website to fit on a smartphone aswell, read more about it [here](https://developer.mozilla.org/en-US/docs/Mobile/Viewport_meta_tag):

		<meta name="viewport" content="width=device-width, initial-scale=1">
		
- Description and keyword meta tags - these tells search engines about the website, read more about it [here](http://searchenginewatch.com/article/2067564/How-To-Use-HTML-Meta-Tags):

		<meta name="description" content="Description" />
		<meta name="keywords" content="Keywords" />


Corrections in this template
----------------------------

If you have suggestions for corrections of this template, then create a new branch and add the corrections or addons in there. Then these corrections/addons will be taking into consideration for the next update.