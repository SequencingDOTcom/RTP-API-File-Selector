# File Selector
Code for adding a File Selector to apps that use [Sequencing.com's](https://sequencing.com/) [Real Time Personalization (RTP)](https://sequencing.com/developer-documentation/what-is-real-time-personalization-rtp) technology. This code is opensource and free to use, share, build upon and improve.

To code Real Time Personalization (RTP) technology into apps, developers may [register for a free account](https://sequencing.com/user/register/) at Sequencing.com. App development with RTP is free.


Contents
=========================================
* Introduction
* Screenshots
* Installation
* Instructions & Endpoints
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

**Sample files list**
* if user selects 'I want to select a sample file' then the list of sample files will appear
* user can select one file
<br>
<br>
![alt tag](https://github.com/SequencingDOTcom/File-Selector-code/blob/master/screenshots/File-Selector-sample-file-view-Sequencing-com.png "Sample files")

**File selected**
* user selected sample file 'Sheila'
* that genetic data in that file will then be used to provide personalized content to the app
* sample files allow user to experience Real-Time Personalization even if they don't yet have their own genetic data
<br>
<br>
![alt tag](https://github.com/SequencingDOTcom/File-Selector-code/blob/master/screenshots/File-Selector-file-selected-view-Sequencing-com.png "User selected sample file 'Sheila'")





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

Instructions & Endpoints
======================================
https://api.sequencing.com/DataSourceList?all=true

This repo contains the code snippet for a File Selector. When added to your app code, the File Selector will allow your app to display a list of files securely stored in the user's Sequencing.com account. Your app user will also be able to use your app to select a file. The selected file will then be used by Sequencing.com whenever your app makes an API request to Sequencing.com.

While using Sequencing.com, a user has the ability to store genetic data files (files that contain data about the user's genes) in different folders. 
* If the app user has files stored at Sequencing.com, this File Selector allows an app to display the app user's files. It also allows the user to select a file to be used when the app sends Sequencing.com an API request. Sequencing.com will then process the API request using the genetic data from the file that the user selected when using this File Selector in your app.
* If the app user does not have files stored at Sequencing.com, this File Selector allows your app to display [fun sample files](https://sequencing.com/knowledge-center/sample-files) provided by Sequencing.com. When using your app, your app user will be able to select one of these sample files and Sequencing.com will then use that sample file data to process all API requests received from your app for that app user.

The user only has to select a file once and thereafter all API requests to Sequencing.com will indicate that this specific file should be used. The user should also have the ability to select a different file at any time. Once a different file is selected, the newly selected file will be used by Sequencing.com to process all incoming API requests from your app.

To learn more about Sequencing.com's API, please see our [App Chains](https://github.com/SequencingDOTcom/App-Chains-Sequencing.com-Real-Time-API) repo.

The default settings for the File Selector will populate the File Selector with all user's files from all of the user's folders at Sequencing.com. If you do not want to use this default setting, you may modify the following endpoints to specify that only files from specific folders should appear in the file selector. If a folder is excluded from an endpoint then the app will not receive any information about files in that folder.

| Folder | Endpoint | Code |
| --- | --- | --- |
| All folders | all=true | https://api.sequencing.com/DataSourceList?all=true 
| My uploaded files | uploaded=true | https://api.sequencing.com/DataSourceList?uploaded=true
| Files shared with me | shared=true | https://api.sequencing.com/DataSourceList?shared=true
| Files saved from my apps | fromApps=true | https://api.sequencing.com/DataSourceList?fromApps=true
| My uploaded files & Files shared with me | uploaded=true&shared=true | https://api.sequencing.com/DataSourceList?uploaded=true&shared=true |
| My uploaded files & Files saved from my apps | uploaded=true&fromApps=true | https://api.sequencing.com/DataSourceList?uploaded=true&fromApps=true |

The File Selector will display files from all of the user's folders using either of the following endpoints (they both return the same information):
* https://api.sequencing.com/DataSourceList?all=true
* https://api.sequencing.com/DataSourceList?uploaded=true&shared=true&fromApps=true

 
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
