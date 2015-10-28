# File Selector
=========================================
Code for adding a File Selector to apps that use [Sequencing.com's](https://sequencing.com/) [Real Time Personalization (RTP)](https://sequencing.com/developer-documentation/what-is-real-time-personalization-rtp) technology. This code is opensource and free to use, share, build upon and improve.

To code Real Time Personalization (RTP) technology into apps, developers may [register for a free account](https://sequencing.com/user/register/) at Sequencing.com. App development with RTP is free.


Contents
=========================================
* Introduction
* Screenshots
* Installation
* Configuration
* Troubleshooting
* Example App
* Maintainers
* Contribute

Introduction
=========================================
The File Selector is JavaScript code that provides a simple, modern file selector for apps that use Sequencing.com's Real-Time Personalization technology. 

Using this code, apps will have the ability to display the genetic data files from the app user's Sequencing.com account. The user will also be able to select one of the files from the list. The genetic data in the user-selected file will then be utilized when providing genetically tailored content.

Screenshots
======================================
**Initial view**
* user can choose to view
 * list of sample files or 
 * list of the user's file's that are stored at the user's Sequencing.com account
<br>
<br>
![alt tag](https://github.com/SequencingDOTcom/File-Selector-code/blob/master/screenshots/File-Selector-initial-view-Sequencing-com.png "Initial view")


**Sample files view**
* if user selects 'I want to select a sample file' then the list of sample files will appear
* user can select one file
* that genetic data in that file will then be used to provide personalized content to the app
<br>
<br>
![alt tag](https://github.com/SequencingDOTcom/File-Selector-code/blob/master/screenshots/File-Selector-sample-file-view-Sequencing-com.png "Sample files")

Installation
======================================
The code is provided in JavaScript and will work with any server side language for all modern web browsers. App developers can cut and paste the code into their apps so that their apps have a file selector that works straight out-of-the-box.

The file selector depends on [Bootstrap](https://github.com/SequencingDOTcom/File-Selector-code/tree/master/bootstrap) and [jQuery 1.11.3+](https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js). 
* Include both of these dependencies prior to using the file selector. 

Review [index.html](https://github.com/SequencingDOTcom/File-Selector-code/blob/master/index.html) for example code to initiate the file selector.

*Installation steps*

1) Include [Bootstrap](https://github.com/SequencingDOTcom/File-Selector-code/tree/master/bootstrap) and [jquery](https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js)

2) Include file selector JS and CSS files from this repo
 * JS file: sequencing-file-selector.js
 * CSS file: style.css

3) Create a hidden input in your form: 
```
<input type="hidden" name="some-name" />
```

4) Initialize the file selector on that form element, using this code: 
```
$('input[type=hidden]').sequencingFileSelector({accessToken: 'the-oauth2-access-token-for-your-app'});
```

Configuration
======================================
There are no strict configurations that have to be performed.

Troubleshooting
======================================
The File Selector code should work straight out-of-the-box without any configuration requirements or issues. 

Other tips

* Ensure that [Bootstrap](https://github.com/SequencingDOTcom/File-Selector-code/tree/master/bootstrap) and [jQuery 1.11.3+](https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js) are installed.
   
* [Developer Documentation](https://sequencing.com/developer-documentation/)

* [oAuth2 guide](https://sequencing.com/developer-documentation/oauth2-guide/)

* Confirm you have the latest version of the code from this repository.

Example App
======================================
What types of apps can you personalize with Real-Time Personalization technology? Any type of app... even a weather app. 
* The open source [Weather My Way +RTP app](https://github.com/SequencingDOTcom/Weather-My-Way-RTP-App/) differentiates itself from all other weather apps because it uses Real-Time Personalization to provide genetically tailored content in real-time to each app user.
* Experience it yourself using one of the fun sample genetic data files. These sample files are provided for free to all apps that use app chains.
* The Weather My Way +RTP app usses the File Selector code from this repo.
 

Maintainers
======================================
The codebase is actively maintained by [Sequencing.com](https://sequencing.com/). Please email the Sequencing.com bioinformatics team at gittaca@sequencing.com if you require any more information or just to say hola.

Contribute
======================================
We encourage you to passionately fork us. If interested in updating the master branch, please send us a pull request. If the changes contribute positively, we'll let it ride.
