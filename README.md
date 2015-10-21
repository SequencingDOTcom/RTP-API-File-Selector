# File Selector
=========================================
Code for adding a File Selector to apps that use [Sequencing.com's](https://sequencing.com/) [Real Time Personalization (RTP)](https://sequencing.com/developer-documentation/what-is-real-time-personalization-rtp) technology. This code is opensource and free to use, share, build upon and improve.

To code Real Time Personalization (RTP) technology into apps, developers may [register for a free account](https://sequencing.com/user/register/) at Sequencing.com. App development with RTP is free.


Contents
=========================================
* Introduction
* Installation
* Configuration
* Troubleshooting
* Maintainers
* Contribute

Introduction
=========================================
The File Selector is code that provides a straightforward file selector for apps that use Sequencing.com's Real-Time Personalization technology. Using this code, apps will have the ability to display the genetic data files from the app user's Sequencing.com account and allow the app user to select one of the files for the app to use when providing genetically tailored content.

Installation
======================================
The code is provided in various coding languages. App developers can cut and paste the code into their apps so that their apps have a file selector that works straight out-of-the-box.

The file selector depends on [Bootstrap](https://github.com/SequencingDOTcom/File-Selector-code/tree/master/bootstrap) and [jQuery 1.11.3+](https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js). 
* Include both of these dependencies prior to using the file selector. 

Review [index.html](https://github.com/SequencingDOTcom/File-Selector-code/blob/master/index.html) for example code to initiate the file selector.

*Installation steps*

1) Include [Bootstrap](https://github.com/SequencingDOTcom/File-Selector-code/tree/master/bootstrap) and [jquery](https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js)

2) Include file selector JS and CSS files from this repo
 * JA file: sequencing-file-selector.js
 * CSS file: style.css

3) Create a hidden input in your form: 
```
<input type="hidden" name="some-name" />
```

4) Initialize the file selector on that form element, using this code: 
```
$('input[type=hidden]').sequencingFileSelector({accessToken: 'the-access-token-for-his-app'});
```

Configuration
======================================
There are no strict configurations that have to be performed.

Troubleshooting
======================================
The File Selector code should work straight out-of-the-box without any configuration requirements or issues. 

Other tips

* Ensure that [Bootstrap](https://github.com/SequencingDOTcom/File-Selector-code/tree/master/bootstrap) and [jQuery 1.11.3+](https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js) are included.
   
* [Developer Documentation](https://sequencing.com/developer-documentation/)

* [oAuth2 guide](https://sequencing.com/developer-documentation/oauth2-guide/)

* Review the [Weather My Way +RTP app](https://github.com/SequencingDOTcom/Weather-My-Way-RTP-App/), which is an open-source weather app that uses Real-Time Personalization to provide genetically tailored content. It uses the file selector code from this repo.

* Confirm you have the latest version of the code from this repository.

Maintainers
======================================
The codebase is actively maintained by [Sequencing.com](https://sequencing.com/). Please email the Sequencing.com bioinformatics team at gittaca@sequencing.com if you require any more information or just to say hola.

Contribute
======================================
We encourage you to passionately fork us. If interested in updating the master branch, please send us a pull request. If the changes contribute positively, we'll let it ride.
