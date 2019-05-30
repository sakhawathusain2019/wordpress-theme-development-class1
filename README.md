# wordpress-theme-development-class1
Here you can find all code information for wordpress theme development here.
<h4>Getting Started</h4>
<p>Ready to start developing WordPress themes? You’re in the right place.</p>
<h4>What is a Theme?</h4>
<p>A WordPress theme changes the design of your website, often including its layout. Changing your theme changes how your site looks on the front-end, i.e. what a visitor sees when they browse to your site on the web. </p>
<h4>What can themes do?</h4>
<p>Themes take the content and data stored by WordPress and display it in the browser. When you create a WordPress theme, you decide how that content looks and is displayed. There are many options available to you when building your theme. For example:
</p>
<ul>
<li>Your theme can have different layouts, such as static or responsive, using one column or&nbsp;two.</li>
<li>Your theme can display&nbsp;content anywhere you want it to be displayed.</li>
<li>Your theme can specify which devices or actions make your content visible.</li>
<li>Your theme can customize its typography and design elements using CSS.</li>
<li>Other design elements like images and videos can be included anywhere in your theme.</li>
</ul>
<p>WordPress themes are incredibly powerful. But, as with every web design project, a theme is more than color and layout. Good themes improve engagement with your website’s content <em>in addition</em> to being beautiful.</p>
<h2 class="toc-heading" id="what-are-themes-made-of" tabindex="-1">What are themes made of? <a href="#what-are-themes-made-of" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text"></span></a></h2>
<p>At their&nbsp;most basic level, WordPress themes are collections of different files that work&nbsp;together to create what you see, as well as how your site behaves.</p>
<h3 class="toc-heading" id="required-files" tabindex="-1">Required files <a href="#required-files" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text"></span></a></h3>
<p>There are only <strong>two files absolutely required in a WordPress</strong> theme:</p>
<ol>
<li><code>index.php</code>&nbsp;–&nbsp;the main template file</li>
<li><code>style.css</code>&nbsp;– the main style file</li>
</ol>
<h2 class="toc-heading" id="template-files" tabindex="-1">Template files <a href="#template-files" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text"></span></a></h2>
<p>WordPress themes are made up of template files. These&nbsp;are PHP files that contain a mixture of HTML, <a title="Template Tags" href="https://developer.wordpress.org/themes/basics/template-tags/">Template Tags</a>, and PHP code.</p>
<p>When you are building your theme, you will use template files to affect the layout and design of different parts of your website. For example, you would use the <code>header.php</code> template to create a header, or the <code>comments.php</code> template to include comments.</p>
<p>When someone visits a page on your website, WordPress loads a template based on the request. The type of content that is displayed in by the template file is determined by the <a href="https://developer.wordpress.org/themes/basics/post-types/">Post Type</a> associated with the template file. &nbsp;The&nbsp;<a title="Template Hierarchy" href="https://developer.wordpress.org/themes/basics/template-hierarchy/">Template Hierarchy</a>&nbsp;describes which&nbsp;template file WordPress will&nbsp;load based on the type of request and whether the template exists in the theme.&nbsp;The server then parses the PHP in the template and returns HTML to the visitor.</p>
<p>The most critical template file is <code>index.php</code>, which is the&nbsp;catch-all&nbsp;template if a&nbsp;more-specific template can not be found in&nbsp;the <a href="https://developer.wordpress.org/themes/basics/template-hierarchy/">template hierarchy</a>.&nbsp;Although a theme only needs a&nbsp;<code>index.php</code> template, typically themes include numerous templates to display different content types and contexts.</p>
<h2 class="toc-heading" id="template-partials" tabindex="-1">Template partials <a href="#template-partials" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text"></span></a></h2>
<p>A template partial is a piece&nbsp;of a template that is included as a part of another template, such as a site&nbsp;header. Template partials can be&nbsp;embedded&nbsp;in&nbsp;multiple templates, simplifying theme creation. Common template partials include:</p>
<ul>
<li><code>header.php</code> for generating the site’s header</li>
<li><code>footer.php</code> for generating the footer</li>
<li><code>sidebar.php</code> for&nbsp;generating&nbsp;the sidebar</li>
</ul>
<p>While the above template files are special-case in WordPress and apply to just one portion of a page, you can create any number of template partials and include them in other template files.</p>
<h2 class="toc-heading" id="common-wordpress-template-files" tabindex="-1">Common WordPress template files <a href="#common-wordpress-template-files" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text"></span></a></h2>
<p>Below is a list of some basic theme templates and files recognized by WordPress.</p>
<blockquote>
<dl>
<dt>index.php</dt>
<dd>The main template file. It is <strong>required</strong> in all&nbsp;themes.</dd>
<dt>style.css</dt>
<dd>The main stylesheet.&nbsp;It is&nbsp;<strong>required</strong>&nbsp;in all&nbsp;themes&nbsp;and contains the information header for your theme.</dd>
<dt>rtl.css</dt>
<dd>The right-to-left stylesheet is included automatically if the website language’s text direction is right-to-left.</dd>
<dt>comments.php</dt>
<dd>The comments template.</dd>
<dt>front-page.php</dt>
<dd>The front page template is always used as the site front page if it exists, regardless of what settings on <strong>Admin &gt; Settings &gt; Reading</strong>.</dd>
<dt>home.php</dt>
<dd>The home page template is the front page by default. If you do not set WordPress to use a static front page, this template is used to show latest posts.</dd>
<dt>header.php</dt>
<dd>The header template file usually contains your site’s document type, meta information, links to stylesheets and scripts, and other data.</dd>
<dt>singular.php</dt>
<dd>The singular template is used for posts when <code>single.php</code> is not found, or for pages when <code>page.php</code> are not found. If <code>singular.php</code> is not found, <code>index.php</code> is used.<p></p>
</dd><dt>single.php</dt>
<dd>The single post template is used when a visitor requests a single post.</dd>
<dt>single-{post-type}.php</dt>
<dd>The single post template used when a visitor requests a single post from a custom post type. For example, <code>single-book.php</code> would be used for displaying single posts from a custom post type named <em>book</em>. The <code>index.php</code> is used if a specific query template for the custom post type is not present.</dd>
<dt>archive-{post-type}.php</dt>
<dd>The archive post type template is used when visitors request a custom post type archive. For example, <code>archive-books.php</code> would be used for displaying an archive of posts from the custom post type named <em>books</em>. The <code>archive.php</code> template file is used if the <code>archive-{post-type}.php</code> is not present.</dd>
<dt>page.php</dt>
<dd>The page template is used when visitors request individual pages, which are a built-in template.</dd>
<dt>page-{slug}.php</dt>
<dd>The page slug template is used when visitors request a specific page, for example one with the “about” slug (page-about.php).</dd>
<dt>category.php</dt>
<dd>The category template is used when visitors request posts by category.</dd>
<dt>tag.php</dt>
<dd>The tag template is used when visitors request posts by tag.</dd>
<dt>taxonomy.php</dt>
<dd>The taxonomy term template is used when a visitor requests a term in a custom taxonomy.</dd>
<dt>author.php</dt>
<dd>The author page template is used whenever a visitor loads an author page.</dd>
<dt>date.php</dt>
<dd>The date/time template is used when posts are requested by date or time. For example, the pages generated with these slugs:<br>
http://example.com/blog/2014/<br>
http://example.com/blog/2014/05/<br>
http://example.com/blog/2014/05/26/</dd>
<dt>archive.php</dt>
<dd>The archive template is used when visitors request posts by category, author, or date. <strong>Note</strong>: this template will be overridden if more specific templates are present like <code>category.php</code>, <code>author.php</code>, and <code>date.php</code>.</dd>
<dt>search.php</dt>
<dd>The search results template is used to display a visitor’s search results.</dd>
<dt>attachment.php</dt>
<dd>The attachment template is used when viewing a single attachment like an image, pdf, or other media file.</dd>
<dt>image.php</dt>
<dd>The image attachment template is a more specific version of <code>attachment.php</code> and is used when viewing a single image attachment. If not present, WordPress will use <code>attachment.php</code> instead.</dd>
<dt>404.php</dt>
<dd>The 404 template is used when WordPress cannot find a post, page, or other content that matches the visitor’s request.</dd>
</dl>
</blockquote>
<h2 class="toc-heading" id="using-template-files" tabindex="-1">Using template files <a href="#using-template-files" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text"></span></a></h2>
<ul>
<li>To include the header, use <tt><a title="Function Reference/get header" href="https://developer.wordpress.org/reference/functions/get_header/">get_header()</a></tt></li>
<li>To include the sidebar, use <tt><a title="Function Reference/get sidebar" href="https://developer.wordpress.org/reference/functions/get_sidebar/">get_sidebar()</a></tt></li>
<li>To include the footer, use <tt><a title="Function Reference/get footer" href="https://developer.wordpress.org/reference/functions/get_footer/">get_footer()</a></tt></li>
<li>To include the search form, use <tt><a title="Function Reference/get search form" href="https://developer.wordpress.org/reference/functions/get_search_form/">get_search_form()</a></tt></li>
<li>To include custom theme files, use <tt><a title="Function Reference/get template part" href="https://developer.wordpress.org/reference/functions/get_template_part/">get_template_part()</a></tt></li>
</ul>
<p>Here is an example of WordPress template tags to&nbsp;<em>include </em>specific templates into your page:</p>

<td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="php plain">&lt;?php get_sidebar(); ?&gt;</code></div><div class="line number2 index1 alt1"><code class="php plain">&lt;?php get_template_part( </code><code class="php string">'featured-content'</code> <code class="php plain">); ?&gt;</code></div><div class="line number3 index2 alt2"><code class="php plain">&lt;?php get_footer(); ?&gt;</code></div></div></td>

<main id="primary" class="site-main post-24939 theme-handbook type-theme-handbook status-publish hentry type-handbook" role="main">

		
		<div class="breadcrumb-trail breadcrumbs" itemprop="breadcrumb">
			<span class="trail-browse">Browse:</span> 
			<span class="trail-begin"><a href="https://developer.wordpress.org" title="WordPress Developer Resources" rel="home">Home</a></span> <span class="sep">/</span> 
			<span class="trail-inner"><a href="https://developer.wordpress.org/themes/">Theme Handbook</a></span> <span class="sep">/</span> 
			<span class="trail-inner"><a href="https://developer.wordpress.org/themes/basics/" title="Theme Basics">Theme Basics</a></span> <span class="sep">/</span> <span class="trail-end">Main Stylesheet (style.css)</span>
		</div>
		
			
<h1>Main Stylesheet (style.css)</h1>


<div class="table-of-contents"><h2>Topics</h2><ul class="items"><li><a href="#location">Location</a></li>
<li><a href="#basic-structure">Basic Structure</a>
<ul>
<li><a href="#example">Example</a>
</li></ul></li>
<li><a href="#style-css-for-a-child-theme">Style.css for a Child Theme</a></li></ul>
</div>
<p>The style.css is a stylesheet (CSS) file required for every WordPress theme. It controls the presentation (visual design and layout) of the website pages.</p>
<h2 class="toc-heading" id="location" tabindex="-1">Location <a href="#location" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text"></span></a></h2>
<p>In order for WordPress to recognize the set of theme template files as a valid theme, the style.css file needs to&nbsp;be located in the root directory of your theme, not a subdirectory.</p>
<p>For more&nbsp;detailed explanation on how to include the style.css file in a theme, see the “Stylesheets” section of <a href="https://developer.wordpress.org/themes/basics/including-css-javascript/#stylesheets">Enqueuing Scripts and Styles</a>.</p>
<p class="toc-jump"><a href="#top">Top ↑</a></p><h2 class="toc-heading" id="basic-structure" tabindex="-1">Basic Structure <a href="#basic-structure" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text">Basic Structure</span></a></h2>
<p>WordPress uses the header comment section of a style.css to display information about the&nbsp;theme in the Appearance (Themes) dashboard panel.</p>
<h3 class="toc-heading" id="example" tabindex="-1">Example <a href="#example" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text"></span></a></h3>
<p>Here is an example of the header part of style.css.</p>
<pre>/*
Theme Name: Twenty Seventeen
Theme URI: https://wordpress.org/themes/twentyseventeen/
Author: the WordPress team
Author URI: https://wordpress.org/
Description: Twenty Seventeen brings your site to life with immersive featured images and subtle animations. With a focus on business sites, it features multiple sections on the front page as well as widgets, navigation and social menus, a logo, and more. Personalize its asymmetrical grid with a custom color scheme and showcase your multimedia content with post formats. Our default theme for 2017 works great in many languages, for any abilities, and on any device.
Version: 1.0
License: GNU General Public License v2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html
Text Domain: twentyseventeen
Tags: one-column, two-columns, right-sidebar, flexible-header, accessibility-ready, custom-colors, custom-header, custom-menu, custom-logo, editor-style, featured-images, footer-widgets, post-formats, rtl-language-support, sticky-post, theme-options, threaded-comments, translation-ready
This theme, like WordPress, is licensed under the GPL.
Use it to make something cool, have fun, and share what you've learned with others.
*/
</pre>
<p>Items indicated with (<em>*</em>) are required for a theme in the WordPress Theme Repository.</p>
<div class="callout callout-info"><p><span class="screen-reader-text">Note:</span> WordPress Theme Repository uses the number after “Version” in this file to determine if the theme has a new version available.</p>
</div>
<ul>
<li><strong>Theme Name</strong> (*): Name of the theme.</li>
<li><strong>Theme URI</strong>: The URL of a public web page where users can find more information about the theme.</li>
<li><strong>Author</strong> (*): The name of the individual or organization who developed the theme. Using the Theme Author’s wordpress.org username is recommended.</li>
<li><strong>Author URI</strong>: The URL of the authoring individual or organization.</li>
<li><strong>Description</strong> (*): A short description of the theme.</li>
<li><strong>Version</strong> (*): The version, written in X.X or X.X.X format.</li>
<li><strong>License</strong> (*): The license of the theme.</li>
<li><strong>License URI</strong> (*): The URL of the theme license.</li>
<li><strong>Text Domain</strong> (*): The string used for textdomain for translation.</li>
<li><strong>Tags</strong>: Words or phrases that allow users to find the theme using the tag filter. A full list of tags is in the <a href="https://make.wordpress.org/themes/handbook/review/required/theme-tags/">Theme Review Handbook</a>.</li>
<li><strong>Domain Path</strong>: Used so that WordPress knows where to find the translation when the theme is disabled. Defaults to <code>/languages</code>.</li>
</ul>
<p>After the required header section, style.css can contain anything a regular CSS file has.</p>
<p class="toc-jump"><a href="#top">Top ↑</a></p><h2 class="toc-heading" id="style-css-for-a-child-theme" tabindex="-1">Style.css for a Child Theme <a href="#style-css-for-a-child-theme" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text">Style.css for a Child Theme</span></a></h2>
<p>If your theme is a Child Theme, the&nbsp;<strong>Template</strong> line is required in style.css header.</p>
<pre>/*
Theme Name: My Child Theme
Template: Twenty Seventeen
*/
</pre>
<p>For more information on creating a Child Theme, visit the <a href="/themes/advanced-topics/child-themes/">Child Themes</a> page.</p>


<div class="bottom-of-entry">&nbsp;</div>

			
		<nav class="handbook-navigation" role="navigation">
			<h1 class="screen-reader-text">Handbook navigation</h1>
			<div class="nav-links">

			<a href="https://developer.wordpress.org/themes/basics/linking-theme-files-directories/" rel="previous"><span class="meta-nav">←</span> Linking Theme Files &amp; Directories</a><a href="https://developer.wordpress.org/themes/basics/organizing-theme-files/" rel="next">Organizing Theme Files <span class="meta-nav">→</span></a>
			</div>
			<!-- .nav-links -->
		</nav><!-- .navigation -->
	
		
		</main>
