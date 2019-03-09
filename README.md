# kali_wordpress
# Project 7 - WordPress Pentesting

Time spent: **X** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Stored XSS
  - [X] Summary: 
    - Vulnerability types: XSS
    Summary: 4.2 version of Wordpress is vulnerable to a stored XSS attack. An unauthenticated attacker can inject JavaScript code in       the Wordpress comments and JS code is executed when comment is viewed by anyone.

    - Tested in version:4.2
    - Fixed in version: 4.2.1
  - [X] GIF Walkthrough: 
  - [X] Steps to recreate: 
      - Add a new post with image which named as XSS alert
      - Add a comment to inject JS code, which should be more than 64 kb.
      - Click on the image, you will see an alert box. 
  - [X] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/changeset?sfp_email=&sfph_mail=&reponame=&new=32311%40branches%2F4.2&old=32300%40branches%2F4.2)
1. (Required) Vulnerability XSS
  - [X] Summary: Admin can run XSS on the page
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.6.1
  - [X] GIF Walkthrough: 
  - [X] Steps to recreate: 
     - Create new page
     - Add the code which triggers XSS alert on load: testing_xss <img src = "#" onerror="alert('xss')">
     
  
1. (Required) Vulnerability Name or ID : USER Enumeration
  - [X] Summary: This exploit allowes user to enumerate through different user names, I tested with multiple non-existing usernames, and        extisting usernames. Upon knowing the valid username or usernames, it is easier to perfrom bruteforce attack. 
    - Vulnerability types: User enumeration
    - Tested in version: 4.2

  - [X] GIF Walkthrough: 
  - [X] Steps to recreate:
    - Try with multiple user names with including the existing usernames
    - See how the response is differ from the non-existing user or existing user. 
 
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2019] [Sushma]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
