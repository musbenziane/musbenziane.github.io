Patrick - vCard / Resume / CV Jekyll Template
---------------------------------------------

By: ducor

Thank you for your purchase. If you have any questions, mail me to - [ducorteam@gmail.com](mailto:ducorteam@gmail.com)

more details ./doc/index.html


*   [File structure](#files_structure)
*   [Install](#install)
*   [RTL Version](#include_rtl)
*   [Background Style](#background_style)
*   [Fonts](#include_fonts)
*   [Icons](#icons)
*   [Credits](#credits)

### Features:

*   \- 4 Background Styles (Image, Color, Particles, Video)
*   \- 6 Color Schemes
*   \- 4 Types Portfolio: Image, Inline, Iframe(YouTube, Vimeo) and Audio(SoundCloud)
*   \- Awesome Portfolio with filters
*   \- Easy to Customize: Colors, Fonts, Content etc..
*   \- HTML5, CSS3 & jQuery powered
*   \- Fully Responsive
*   \- Valid, Clean and Commented code
*   \- Cross browser
*   \- Minimal and Clean
*   \- LESS CSS Included
*   \- Fully Working Contact Form PHP
*   \- Blog Post Page
*   \- Blog Page List and Sidebar
*   \- 20+ Popular Social Icons
*   \- 200+ Fonts Icons
*   \- LineAwesome Icons
*   \- Google Fonts
*   \- Google Maps
*   \- jQuery Validation Plugin
*   \- CSS3 Animations
*   \- Pricing Tables
*   \- Regular Updates
*   \- 24/7 Support
*   \- RTL Version Support Included
*   \- Documentation included

Install Template
----------------

After unzip the download pack, you'll found a Template Folder with all the files.

To use this project, you'll need the following things installed on your machine.

1\. \[Jekyll\] (http://jekyllrb.com/) - `$ gem install jekyll bundler`

Start Jekyll server on your local machine `$ Bundle exec jekyll serve` Injoy

Basic
-----

To keep your sanity and better manage dependencies I strongly urge you to install Bundler with gem install bundler and use the following Gemfile:

You can view this Template in any browser, you can display or edit the Template without an internet connection.(May not wotrk fonts and google map).

This section that will not work is the Contact Section which contains formspree.io form service for send messages.

Now go to your github account and create repository (name like `yourname.github.io`). Push the content of the Template on your github repo.

Once the files are done uploading go to `yourname.github.io`

Enjoy

Install Template
----------------

To use this project, you'll need the following things installed on your machine.

1\. \[Jekyll\] (http://jekyllrb.com/) - `$ gem install jekyll bundler`

Start Jekyll server on your local machine `$ Bundle exec jekyll serve` Injoy
                       

Jekyll Template structure
-------------------------

After unpacking archive, you'll see this structure:

    
    main
    ├───blog
    ├───css
    │   └───theme-colors
    ├───doc
    │   └───assets
    ├───fonts
    ├───images
    │   ├───blog
    │   ├───clients
    │   ├───favicons
    │   └───works
    ├───js
    ├───less
    │   └───theme-colors
    ├───video
    ├───_data
    │   └───sections
    ├───_includes
    │   ├───analytics-providers
    │   ├───comments-providers
    │   └───sections
    ├───_layouts
    ├───_posts
    
    						

*   css - all CSS for pages
    *   basic.css - CSS for basic styles
    *   layout.css - CSS for template layout
    *   blogs.css - CSS for blog post
    *   rtl.css - CSS for rtl support
    *   theme-colors/ - CSS files for template colors
*   less - all LESS for pages
    *   setting.less - LESS for setting template
    *   basic.less - LESS for basic styles
    *   layout.less - LESS for template layout
    *   blogs.less - LESS for template Blog
*   js - all JS for pages
    *   scripts.js - Main JS for template


Colors Schemes
--------------

Just change on you ./\_config.yml file. "(green.css blue.css, orange.css, red.css, pink.css, purple.css)"

    
    color_scheme: "green" # "green" (default), "blue", "orange", "pink", "purple", "red"
    
    					

./includes/head.html

    
    <!-- theme colors -->
    
    <link rel="stylesheet" href="{{ 'css/theme-colors/{{ site.color_scheme }}.css' | relative_url }}" />
    	
    					

RTL Version
-----------

Just add "rtl.css" at the ./includes/head.html file:

Your need to change ./\_config.yml file

    
    html_dir:  'rtl' # ltr ( default ), "rtl"
    					

    
    	
    	{%- if site.html_dir == 'rtl' || page.html_dir == 'rtl' -%}
    	<link rel="stylesheet" href="{{ 'css/rtl.css' | relative_url }}" />
    	{%- endif -%}
    					

Background Style or Home Card
-----------------------------

4 Background Styles (Image, Color, Particles, Video)

Your need to change ./\_config.yml file

    
    home_style:  'background-image' # "background-image" (default), "background-color", "particles-bg", "video-bg"
    
    					

./includes/sections/home-card.html

    
    
    <!--
    	Card - Started
    -->
    <div class="card-inner card-started active" id="home-card">
    	{%- if site.home_style == 'background-image' -%}
    		<div class="slide" style="background-image: url({{ 'images/bg.jpg' | relative_url }});"></div>
    	{%- elsif site.home_style == 'background-color' -%}
    		<div class="slide" style="background-color: #242425;"></div>
    	{%- elsif site.home_style == 'particles-bg' -%}
    		<div id="particles-bg" class="slide" style="background-image: url({{ 'images/bg.jpg'| relative_url }});"></div>
    	{%- elsif site.home_style == 'video-bg' -%}
    		<div id="video-bg" class="slide" data-property="{videoURL:'https://youtu.be/S4L8T2kFFck', containment:'#video-bg', showControls:false, autoPlay:true, loop:true, mute:false, startAt:0, opacity:1, addRaster:true, quality:'default'}"></div>
    	{%- else -%}
    		<div class="slide" style="background-image: url({{ 'images/bg.jpg' | relative_url }});"></div>	
    	{%- endif -%}
    	<div class="centrize full-width">
    		<div class="vertical-center">
    
    			<!-- Started titles -->
    			<div class="title"><span>{{ site.first_name }}</span> {{ site.last_name }}</div>
    			<div class="subtitle">
    				I am 
    				<div class="typing-title">
    					{%- for profession in site.professions -%}
    					<p>a <strong>{{ profession }}.</strong></p>
    					{%- endfor -%}
    				</div>
    				<span class="typed-title"></span>
    			</div>
    			
    		</div>
    	</div>
    </div>
    						
    
    					

Include of fonts
----------------

To use fonts, you must add one tag 'link' from section below to head section.

    
    <link href="https://fonts.googleapis.com/cssfamily=Poppins:100,100i,200,200i,300,300i,400,400i,500,500i,600,600i,700,700i,800,800i,900,900i" rel="stylesheet">
    					

Next step is to set the @default-font option with using settings table.

Home Page structure
-------------------

```
    ---
    layout: home
    keywords: [vcard, resposnive, resume, personal, card, cv, cards, portfolio]
    ---
```
    	

Icons
-----

In this template are defined some of classes for icons, your can see all icons here - https://icons8.com/line-awesome

Sourse & Credits
----------------

### Scripts

*   Animate.css [https://daneden.github.io/animate.css/](https://daneden.github.io/animate.css/)
*   jQuery [https://jquery.com/](https://jquery.com/)
*   Masonry [https://masonry.desandro.com/](http://masonry.desandro.com/)
*   imagesLoaded [http://imagesloaded.desandro.com/](http://imagesloaded.desandro.com/)
*   jQuery Validation Plugin [http://jqueryvalidation.org/](http://jqueryvalidation.org/)
*   Magnific Popup [http://dimsemenov.com/plugins/magnific-popup/](http://dimsemenov.com/plugins/magnific-popup/)
*   Masonry Filter [https://github.com/dynamick/multiple-filter-masonry](https://github.com/dynamick/multiple-filter-masonry)
*   SimpleBar [https://grsmto.github.io/simplebar/](https://grsmto.github.io/simplebar/)
*   Particles.js [https://github.com/VincentGarreau/particles.js](https://github.com/VincentGarreau/particles.js)
*   Typed.js [https://mattboldt.com](https://mattboldt.com)
*   jquery.mb.YTPlayer [https://github.com/pupunzi/jquery.mb.YTPlayer](https://github.com/pupunzi/jquery.mb.YTPlayer)
*   Jekyll - [https://jekyllrb.com](https://jekyllrb.com)

### Fonts

*   Poppins [https://fonts.google.com/specimen/Poppins](https://fonts.google.com/specimen/Poppins)
*   LineAwesome - [https://icons8.com/line-awesome](https://icons8.com/line-awesome)

### Images

Any Images or logos used in previews are not included in this item or final purchase.

*   Unsplash [https://unsplash.com/](https://unsplash.com/)
*   Graphicburger [http://graphicburger.com/](http://graphicburger.com/)