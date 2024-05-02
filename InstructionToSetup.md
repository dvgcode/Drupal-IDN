# IDN implementation on Drupal CMS version 10.2.5


## Setup
This repository is a clean installation for latest version of Drupal CMS version 10.2.5.

### Pre-requisite
WebServer: Apache/2.4.54 (Win64)
PHP version : PHP/8.1.10 
MySQL : MySQL 8.0.30 / MariaDB 10.
Operating System  : Windows & Linux (Ubuntu)

### Database Setup

Create a new database.
'''
CREATE DATABASE `drupal10_idn` /*!40100 COLLATE 'utf8mb3_general_ci' */;
''' 


Check available database in local machine
'''
SHOW DATABASES;
'''

To use database
'''
USE `drupal10_idn`;
'''

Import .sql file available db directory in current repository branch to create database.


### Installation Steps

Drush - For cleaning cache

Admin Panel Credentials
admin / @dm!n@123$%^


### Language Setup
Admin > configuration > Region & Language > 


### Content Creation
Steps in document. One Page Creation
Bi-lingual Language Setup

### Language Switch Component
Using  Language Switcher Dropdown component downloaded from 

### Host File Setup
Host file setup is a pre-requisite for URL change functionality equivalent to DNS setup.

To enable IDN implementation in local machine need to add following entry (respective domain name) in C:\Windows\System32\Drivers\hosts file

'''
127.0.0.1 example.com
127.0.0.1  उदाहरण.भारत
'''

### IDN Implementation
In order to change IDN URL, based on language change using language switch module, following cod esnippet need to be added using JavaScript as follows:

```
<script>
window.onload = function(){
  var lang = document.getElementById('edit-lang-dropdown-select').value;
  if(lang == 'hi'){
      location.assign('http://उदाहरण.भारत/Drupal-IDN/web/hi/')
  }else{
    location.assign('http://example.com/Drupal-IDN/web/en-gb/')
  }
}
</script>
```


### Cache Clear
To clear cache in Drupal CMS for any change, go to admin link to clear cache
/admin/config/development/performance