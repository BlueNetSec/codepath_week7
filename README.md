# Project 7 - WordPress Pentesting

Time spent: **3** hours spent in total

> Objective: Find, analyze, recreate, and document **three vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. Vulnerability Name: Cross site scripting  
  - [ ] Summary:In WordPress 4.2, an attacker can inject JavaScript in 
WordPress comments. The script is triggered when the comment is viewed.
    - Vulnerability types:XSS
    - Tested in version: 4.2
    - Fixed in version:  4.6
  - [ ] GIF Walkthrough:
  
  
  ![1](https://user-images.githubusercontent.com/24555370/31864921-e4a6ec18-b733-11e7-8d18-aa71ec06f50f.gif)
  - [ ] Steps to recreate: 
      -  1. Create a new post
      - 2. Open the post and insert <script>alert("XSS")</script> on comment section
      - 3. Whenever the post is opened, xss expolited script is run.
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/c9e60dab176635d4bfaaf431c0ea891e4726d6e0)
    
    
 2. Vulnerability Name: Cross site scripting in update plugin  
  - [ ] Summary:In WordPress 4.2, attackers can inject arbitrary web script or HTMLto update-core.php. 
    - Vulnerability types:XSS
    - Tested in version: 4.2
    - Fixed in version:  4.7
  - [ ] GIF Walkthrough:
  
  ![2](https://user-images.githubusercontent.com/24555370/31865574-d5107ed0-b73e-11e7-9008-c330b7aedb60.gif)
  - [ ] Steps to recreate: 
      -  1. Edit a plugins name to <script>alert("XSS");</script>
      -  2. Whenever the Update page is opened, xss expolited script is run.
  - [ ] Affected source code:
    - [Link 2](https://core.trac.wordpress.org/browser/trunk/src/wp-includes/shortcodes.php)
 
 3. Vulnerability Name: Authenticated Shortcode Tags Cross-Site Scripting
  - [ ] Summary: reference:https://wpvulndb.com/vulnerabilities/8186
  
    - Vulnerability types:XSS
    - Tested in version: 4.2
    - Fixed in version:  4.3
  - [ ] GIF Walkthrough:
 
 ![3](https://user-images.githubusercontent.com/24555370/31865942-7bb7b3d8-b745-11e7-9dc7-7a39b3d6267c.gif)

  - [ ] Steps to recreate: 
      -  1. Insert SHORT CODE[caption width="1" caption='<a href="' ">]</a><a href="http://onMouseOver='alert("shor code")'">Click me</a> payload placed in a page or post
      -  2. Whenever the page is opened, xss expolited  is run.
  - [ ] Affected source code:
    - [Link 3](https://github.com/WordPress/WordPress/commit/f72b21af23da6b6d54208e5c1d65ececdaa109c8)
    

