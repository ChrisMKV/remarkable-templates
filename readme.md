# ReMarkable Templates
Templates for my ReMarkable tablet.

## How to use
See:

https://www.simplykyra.com/learn-how-to-access-your-remarkable-through-the-command-line/
https://www.simplykyra.com/how-to-make-template-files-for-your-remarkable/#upload-the-template-image

Git repo on my Mac at: /Users/chris/Repos/remarkable-templates

### Connect to Remarkable
Plug the ReMarkable to the PC with USB. On the ReMarkable, go to Settings > Help > Copyrights and licenses. The connection info is at the bottom of the page.

Open the terminal and connect with *root*:
````
ssh root@x.x.x.x
````

### Copy files from the ReMarkable to the repo
This step may be required after updates to ensure the default templates are up-to-date in the repo. Run the command from the Mac, not the ReMarkable:
````
scp -r root@x.x.x.x:/usr/share/remarkable/templates/ /Users/chris/Repos/remarkable-templates
````

### Copy files from repo to the ReMarkable
Remember to update the *templates.json* file before uploading the files to the ReMarkable.
````
scp -r /Users/chris/Repos/remarkable-templates/templates root@x.x.x.x:/usr/share/remarkable/
````

### Apply changes
After uploading the changes, restart the ReMarkable or restart the *xochitl* with this command:
````
systemctl restart xochitl
`````