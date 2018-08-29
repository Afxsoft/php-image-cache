# Image Cache v. 2.0

Image Cache is a very simple PHP class that accepts an image source and will compress and cache the file, move it to a new directory, and returns the new source for the image.

## Installation

Install <a href="http://getcomposer.org" target="_blank">Composer</a> by opening Terminal and navigating to the directory in which you'd like to install Image Cache.

Installation
Execute this bash command from your project’s root directory:
```bash
composer require afxsoft/phpimagecache:dev-master
```
Basic Usage
The class is pretty small, and very basic. First, include the file and initialize the class:
```bash
require_once 'ImageCache.php';
$imagecache = new Afxsoft\App\ImageCache();
```
Optional: Set the location of the directory to house your cached images:
```bash
$imagecache->cached_image_directory = dirname(__FILE__) . '/images/cached';
```
Next, reference the image that you want compressed and store the new image source in a variable. Echo this variable within the 'src' attribute of an image tag:
```bash
$cached_src = $imagecache->cache( 'images/unsplash1.jpeg' );
/// <!-- later in your HTML -->
<img src="<?php echo $cached_src; ?>" alt="Amazingly awesome photo">
```
