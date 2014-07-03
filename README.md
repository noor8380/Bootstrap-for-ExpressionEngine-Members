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

###Template Snippets
You'll want to create a pair of snippets in your EE install named `Global Header` and `Global Footer`. I've already included the references to these in the templates and use those files to as the wrapper for the members area. Attempting to do so with the `html_header.html` and `html_footer.html` files will result in the popup functions acting all wonky. Don't blame me, this is how EE calls that shit, a future update will have some sort of workaround to turn those into proper Bootstrap modals.

###Notes
This is far from finished. Some of the code is sloppy since I basically just ripped this out of an existing project, and I'm still cleaning it up to be more of a "universal" distribution.

