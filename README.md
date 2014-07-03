#Bootstrap Theme for EE Members
This project is a basic skin for ExpressionEngine's Members module that uses Bootstrap classes. Don't waste precious manhours trying to start from scratch or dealing with EE's default templates - Swap in these files with Bootstrap and knock out like 80% of the UI work in one fell swoop!

They're intentionally bare-bones so you can work in your own customizations. It should be compatible with *most* Bootstrap themes from the get-go, though I've only tested it with the default and [Bootswatch's Cosmo theme](http://bootswatch.com/cosmo/).

I guess it goes without saying that this will not work without Bootstrap. You can grab the latest version at [getbootstrap.com](http://getbootstrap.com).

###Implementation
Upload the full contents of `/bootstrap/` to `/themes/profile_themes/`, then in your admin panel, set Bootstrap as the default theme in your global member preferences.
```
{exp:wiki base_path='wiki/index' wiki="INSERT WIKI SHORTNAME HERE" theme="bootstrap"}
```
Then just point your browser to `yoursiteurl.com/wiki/` and there you go.

If you are using the Multiple Site Manager and want each site to have separate themes, just duplicate the `/bootstrap/` folder, and declare the new folder's name in that site's member preferences.

**Also**, don't forget to fill in lines 6, 7, and 8 in `html_header.html` with the full paths to your local Bootstrap files (or CDN-hosted files).

You should also go to line 22 of `public_profile.html` and fill in your install's channel names, site names, and statuses, otherwise the 'latest posts' loop of the profile won't work. (If you don't plan on using it, you can always remove it.)

###Template Snippets and Global Variables
You'll want to create a snippet in your EE install named `global_footer`. I've already included the references to this in the appropriate templates. You can use that snippet and the `page_header.html` file as the wrapper for the members area. Attempting to do so with the `html_footer.html` file will result in the popup functions acting all wonky. Don't blame me, this is how EE calls that shit, a future update will have some sort of workaround to turn those into proper Bootstrap modals.

You'll also want to create a pair of Global Variables: `text_tos` and `text_whyregister`. The login and registration forms call these - fill in whatever your sales pitch and terms of service for your members is going to be in those snippets.

###Notes
This is far from finished. Some of the code is sloppy since I basically just ripped this out of an existing project, and I'm still cleaning it up to be more of a "universal" distribution.

