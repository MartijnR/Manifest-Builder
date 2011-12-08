Manifest Builder (for Code Igniter)

by: Martijn van de Rijdt (Aid Web Solutions)
https://github.com/MartijnR/Manifest-Builder


Description:

This class dynamically creates a manifest file that contains a list of the resources for the browser's Application Cache. Using an Application Cache will speed up loading times and make the application available offline. Both HTML5 and Gears (deprecated) manifest formats are supported. The manifest will automatically generate a new 'version number' when any of the resources have changed to inform the browser to update the Application Cache.

The builder is implemented as a fat controller to keep things simple (and I can't think of a situation where you'd have more than 1 manifest in an application). 


How to use:

If using Code Igniter's (excellent) PHP framework, this controller can simply be copied into the application/controllers folder. To test go to: yourdomain.com/manifest/html5 (or yourdomain.com/manifest/gears). If it works add the manifest url to your html.  If another PHP framework is used you'll have to tweak the code (become a collaborator and post your port here!).

The commented block right after the class declaration allows customization of the manifest and includes:

- a forced version number update ($hash_manual_override) in case this is necessary (e.g. when edits in server code do not necessarily change the generated client resources and thus do not change the hash (version))

- adding additional resources-to-be-cached ($pages), such as any pages in addition to the root ('')

- the page to load when an app is offline and gets a request for a page that does not exist in the Application Cache ($offline)

- any resources that should never be cached ($network)


I am just starting to code and this is my first open source contribution. ANY SUGGESTIONS to improve the code are very welcome!





