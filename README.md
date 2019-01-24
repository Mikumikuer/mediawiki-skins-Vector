Vector Skin
========================

Configuration options
---------------------

### $wgVectorPrintLogo

Logo used in print styles. Keys are `url`, `width`, and `height` (in
pixels). Note that this solution only works correctly if the image
pointed to by `url` is an SVG that does not specify width and height
attributes, or its width and height match the corresponding variables
below. Alternatively, a PNG or other type of image can be used, but
its dimensions also need to match the corresponding variable below.
That in turn may result in blurry images, though.

The URL can be absolute or relative.

Example configuration:

	$wgVectorPrintLogo = [
		'url' => 'https://en.wikipedia.org/static/images/mobile/copyright/wikipedia-wordmark-en.svg',
		'width' => 174,
		'height' => 27
	];

* Type: `Array`
* Default: `false`

MenuSidebar Modify
---------------------

Create your own wikitext based sidebar

add `$wgVectorMenuSidebar = true;` in `LocalSettings.php` to activate MenuSidebar.

Sidebar style is built in backend, edit ./components/MenuSidebar.less to customize MenuSidebar.

example for `Mediawiki:MenuSidebar` by default style settings:

	MenuTitle #1
	* '''NotLink Item must use Boldtext tag''' 
	** [externalLink Item]
	*** [[Item]]
	MenuTitle #2
	* [[Link Item]]
	** '''NotLink Item'''
	*** [[Item]]
	**** [[item Level can be infinite]]
	{{#Parser Function Item}}

Example site with MenuSidebar: [www.gfwiki.org]
