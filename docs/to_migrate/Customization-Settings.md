## Application Name
This will change most references to the word `Ombi` to a new name, this includes on the website (need to refresh the browser), and in notifications. 

## Application Url
This is for any external links we send out (this link should be the externally accessible URL), usually in the form of an email.
e.g. Password reset email - we use the Application URL to take them to a page where they can reset their password. 

#### Format:
`http://ombi.io/`

## Custom Logo
This is used for the Login Page, Landing Page and also any notifications that we send a logo e.g. Email Notifications

#### Format:
`http://url.to.picture/`

## Custom CSS  
There are two ways we officially support custom CSS.
They are by import or direct entry.
For some ideas, you can find some common customisations under [V4 Custom Themes](https://github.com/tidusjar/Ombi/wiki/Ombi-v4-Custom-Themes)<br>
Any CSS you wish to use should be put into the Custom CSS box. It could be a reference to a CSS file (via an import reference) or could be raw CSS itself.

### CSS Import
Please note, this requires a MIME type of `text/css` or the browser will not load it as a stylesheet.<br>

## Custom Donation
We have the ability to set a custom donation url and message, this will be displayed to all users unlike the ombi donation message.

## Use Custom Page
This allows you to add a blank page to the Nav bar that you are able to fully customise the HTML with a WYSIWYG editor.
Once you enable this setting, just refresh the page and you will see the new option in the navigation bar, from there you can edit your page.

**Note:** You must add the _Edit Custom Page_ Role to your user account before you are able to edit the Custom Page.
This can be done via the `User Management` page.   

**Disclaimer**: The _Custom Page_ is public and can be accessed without authorization, there are plans to add an authorization toggle to this page.  Use the custom page with caution.   

## Landing/Login Page Backgrounds
We do have the ability to change what backgrounds are used on the landing and login pages.

This is not done via the Ombi UI, but done in the `appsettings.json` file in the Ombi directory [Example.](https://github.com/tidusjar/Ombi/blob/master/src/Ombi/appsettings.json)

If you look at that file you can see the following sections:

```
"LandingPageBackground": {
    "Movies": [
      278,
      244786,
      680,
      155,
      13,
      1891,
      399106
    ],
    "TvShows": [
      121361,
      74205,
      81189,
      79126,
      79349,
      275274
    ]
  }
```

The numbers are TheMovieDbId's for Movies and TvDbId's for Tv Shows.
You are able to add/remove the Id's for the sections to change the background images.
If you do not want any TV shows or Movies then leave that section as an empty array e.g.

```
"LandingPageBackground": {
    "Movies": [
      278,
      244786,
      680,
      155,
      13,
      1891,
      399106
    ],
    "TvShows": []
  }
```

The above will only show movie backgrounds.