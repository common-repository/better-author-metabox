=== Plugin Name ===
Contributors: shooflydesign
Tags: admin, users
Requires at least: 3.5
Tested up to: 5.3
Stable tag: 1.0.5
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Lets you safely override the built-in Author metabox with one that includes more users.

== Description ==

This plugin can override the Authors metabox on the post add/edit screen, letting users who can edit other people's posts, reassign a post to others user on the site.

This is especially useful in situations where you've created custom user roles that WordPress doesn't recognize as Authors.  If you want to allow your content editors and administrators to assign new or existing content to anyone, you'll (hopefully) like this plugin very much indeed.

On WordPress 5.0, the metabox will appear below the main block editor (see screenshot).  I will be supporting updates to the Status & Visibility box as soon as possible.

I'm not sure how far back this plugin will work, I'm saying it requires 3.5 or greater — it was originally developed using WordPress 4.1.

(Inspired by [this trac ticket](https://core.trac.wordpress.org/ticket/18645))

== Installation ==

1. Upload the `better-author-metabox` folder to the `/wp-content/plugins/` directory
1. Activate the plugin through the 'Plugins' menu in WordPress
1. Visit Settings > Better Author Metabox to choose the post types where the expanded Author metabox should be made available, and users who should be included.

== Frequently Asked Questions ==

= I don't see any difference.  What gives? =

There are at least three reasons:

1.  To see the better metabox, the logged-in user must have the `edit_others_posts` capability.  If you can't edit other people's posts, you shouldn't be able to change a post's author, right?

1.  You need to choose the post types where the plugin should be enabled.  **None are enabled by default.**  If a post type hasn't been enabled, it will use the default metabox.

1.  If you've enabled a post type to use the better metabox, but still only see authors, select additional user roles to make sure they're included in the dropdown.  This is especially useful for custom roles you've created.

= Can I exclude certain users without using roles? =

This plugin doesn't support that directly, but there is a filter (`bam_wp_dropdown_users`) that works just like the core `wp_dropdown_users` filter to let you edit its HTML before output.

== Screenshots ==

1. The settings screen.  You'll want to check some of these boxes or the plugin won't do anything!

1. The metabox appears beneath the main block editor window in WordPress 5.0 and up, along with other metaboxes using the longstanding metabox APIs.

== Changelog ==

= 1.0 =
* Initial version.

= 1.0.1 =
* Fixed issue with multiple roles not being correctly merged (hat tip: WPSeeker), and a couple small issues with settings.

= 1.0.2 =
* Fixed issues in PHP strict mode (hit tip: Clifford Paulick), and other spots where notices and warnings might appear.

= 1.0.3 =
* Tested with WordPress 5.0's Gutenberg block editor, updated documentation.

= 1.0.4 =
* Code style fixes, tested on WordPress 5.1.

= 1.0.5 =
* Tested on WordPress 5.3.
