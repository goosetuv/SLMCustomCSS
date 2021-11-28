# SnowLicenseManager-CustomCSS
Fully documented and working custom.css and relevant files for Snow License Manager to make it your own.

![Screenshot of the SnowLicenseManager Snowboard with Custom CSS](/Images/customCSS_Snowboard.png)

__Note__ the above image is from an incomplete version of the CustomCSS.

## Pre-warning
Certain areas of Snow License Manager cannot have their colour changed without modifying the sprite PNG, or creating your own sprite PNG entirely.  As I'm unsure if this breaks the EULA, I have not included these files, however you can modify them yourself by copying `snow-ui-sprite.png` from `C:\Program Files\Snow Software\Snow License Manager\Web\Content\Images\` in the Snow License Manager installation folder, open it in [photoshop](https://www.adobe.com/uk/products/photoshop/), [gimp](https://www.gimp.org/) or [paint.net](https://www.getpaint.net/) and going wild on editing the blue out.  Don't open it in MS Paint because it'll lose any transparency. 

For an extensive list of things I found that I can't change, please refer to [known issues](KNOWNISSUES.MD). 

## Custom Branding
You might find that your company colours don't work directly out the box with this, if you need any help with certain elements needing their colours changed outside of the 'standard' customization (i.e updating `root { }`), raise an issue and I'll give you some assistance.  This is the first release of this repo, so some things might not be perfect yet.

## Usage
Setting this up is pretty simple, you just need to make sure you have Administrator rights on the Snow License Manager server (not the portal, just the server.)

### custom.css
Go to `C:\Program Files\Snow Software\Snow License Manager\Web\content\styles\` and replace `custom.css` with the one from here.

### lm-custom
`lm-custom` is where some custom images and the updated logos are stored.

To update your logo across the platform, please refer to the files within `lm-custom/logos` or read the [Logo](#logo) section.

That's it.  Afterwards it should look something like this:

![Screenshot of Styles directory](/Images/lm-styles.png)
![Screenshot of Content directory](/Images/lm-custom.png)

### Modification
#### Colours
If you want to change the colour from [#goffsnow](/Images/goffsnow.png), you can edit the `:root { }` element at the top of the `custom.css` file from the repo. Outside of the things mentioned in [Pre-warning](#pre-warning), it'll update the colours across the entire platform.

#### Logo
To change the logo, there are three files within the `lm-custom/logos` directory, you can either replace these with same size images, or you can modify the classes at the top of `custom.css`

`.swui-about-system .logo-holder { }`, `.logo-container .logo-holder, .hd-TopNav_LogoItem .logo-holder { }` and `.login_body .logo-container .logo {  }`

The ideal sizing for each logo is

- **Login Page**: 350x34
- **Nav Bar**: 247x24
- **About Page**: 420x41

## Versioning
The versioning of this repo follows the versioning of Snow License Manager.  I.E 9.16, 9.17 etc. to make it easier for people to understand which release they need, and which release the customization was last tested on.

## Contributing
Happy for anyone to contribute, take a fork and push through some requests if you think we can make this better. 
