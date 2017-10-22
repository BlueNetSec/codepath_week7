# Project 7 - WordPress Pentesting

Time spent: **X** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

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
        1. Create a new post
        2. Open the post and insert <script>alert("XSS")</script> on comment section
        3. Whenever the post is opened, xss expolited script is run.
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/c9e60dab176635d4bfaaf431c0ea891e4726d6e0)
    
    

