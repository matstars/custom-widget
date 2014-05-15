Custom Widget
===================
Contributors: matstars, voceplatforms  
Tags: post, widget  
Tested up to: 3.9.1  
Requires at least: 3.6  
Stable tag: 0.1.3  
License: GPLv2 or later  
License URI: http://www.gnu.org/licenses/gpl-2.0.html  
  
  
## Description
Provides a widget that allows you to output a title, a call to action (CTA) text with a link, textarea and an image. It comes with a prebuilt template, but you can easily extend it using filters and add your own template on a global basis and/or a per-widget basis.

## Installation
> See [Installing Plugins](http://codex.wordpress.org/Managing_Plugins#Installing_Plugins).


## Usage

#### Usage of cw_template filter

Add a template directory and file named "custom-cw.php" to your template directory. The "custom-cw.php" file will be your custom template for this example, see below.

#### Example of using a custom template from within your theme pre-PHP 5.3

```php
<?php
    function customize_cw_template_filter( $template ){
        $template_dir = get_template_directory();
        return $template_dir . '/views/custom-cw.php';    
    }
    add_filter( 'cw_template', 'customize_cw_template_filter' );
?>
```


#### Example of using a custom template from within your theme PHP 5.3+ which allows anonymous functions

```php
<?php

    add_filter( 'cw_template', function( $template ){
        $template_dir = get_template_directory();
        return $template_dir . '/views/custom-cw.php';
    });
?>
```


## Changelog

**0.1.3**
* Bugfixes, sanitization and escaping all the things

**0.1.2**
* Incremental bugfixes

**0.1.1**
* Incremental bugfixes

**0.1.0**  
* Initial release
