# Wordpress Line Awesome Icon Set

## About
This is not an official extension and I am not the owner of these icons.

Official owner of icons:
https://icons8.com/line-awesome


Pre-made configuration to use Line Awesome icon set in Wordpress editor. I believe it can help someone.

## How It Works

It works together with the Icon Block plugin, which can be found directly in the Wordpress plugin repository: 
https://wordpress.org/plugins/icon-block/

## Installation

Before you can use the plugin, you need to register the register.js script with the code below (you can also read the instructions on nickdiego.com)

```
function register_line_awesome_icon_set() {
	wp_enqueue_script(
		'line-awesome-icon-set',
		get_stylesheet_directory_uri() . '/js/icons/register.js' ,
		array( 'wp-i18n', 'wp-hooks', 'wp-dom' ),
		'1.0.0',
		true // Very important, otherwise the filter is called too early.
	);
}

add_action( 'enqueue_block_editor_assets', 'register_line_awesome_icon_set' );
```
This snippet is designed to load script from theme folder, supporting also child themes.

More detailed instructions on how this works:

https://nickdiego.com/adding-custom-icons-to-the-icon-block/
