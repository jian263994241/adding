##Usage
IE7.js
Upgrade MSIE5.5-6 to be compatible with MSIE7.

	<!--[if lt IE 7]>
	<script src="http://ie7-js.googlecode.com/svn/version/2.1(beta4)/IE7.js"></script>
	<![endif]-->
IE8.js
Upgrade MSIE5.5-7 to be compatible with MSIE8.

	<!--[if lt IE 8]>
	<script src="http://ie7-js.googlecode.com/svn/version/2.1(beta4)/IE8.js"></script>
	<![endif]-->
You do not need to include IE7.js if you are using IE8.js

IE9.js
Upgrade MSIE5.5-8 to be compatible with modern browsers.

	<!--[if lt IE 9]>
	<script src="http://ie7-js.googlecode.com/svn/version/2.1(beta4)/IE9.js"></script>
	<![endif]-->
You do not need to include IE7/IE8.js if you are using IE9.js

PNG
The script only fixes images named: *-trans.png

If you want the fix to apply to all PNG images then set a global variable as follows:

	var IE7_PNG_SUFFIX = ".png";
You must set this variable before including the IE7.js script. Alternatively, you can set the variable inside the IE7.js script element:

	<script src="IE8.js">IE7_PNG_SUFFIX=".png";</script>
The suffix will ignore query string parameters. For more fine-grained control you can also set IE7_PNG_SUFFIX to a RegExp object. If you want to use an alternative PNG solution then set the suffix to something that cannot possibly match:

	var IE7_PNG_SUFFIX = ":";
By default, the PNG will be stretched (this simulates tiling). If you want to turn this off then set the no-repeat property as follows:

	div.example {
	  background: url(my-trans.png) no-repeat;
	}
Unfortunately, the transparent background image cannot be tiled (repeated) using background-repeat. Nor can it be positioned using background-position.