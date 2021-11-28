# Known Issues
This is a list of 'known issues', i.e Snow have used an image that is already colored instead of using raw css.  These items need to have this image replaced for their color to be updated.

This isn't an extensive list, but it should cover most things.  If you find anything else please raise it as as a merge request and we can update the list as we go.

## Site Wide
### Loading Gif
The loading gif that is used across the platform has a blue background saved into the gif.  The loading icon needs to be replaced to change the color, this is located here `Images/loader-main-slm15.gif`

Class for the login page specifically is `.login_body .loading` and already in `custom.css`. 

Gifs that need replaced

- `/Images/swui-loader-fallback.gif`
- `/Images/loader-main-slm15.gif`
- `/Images/loader-white-bg-md.gif`
- `/Images/loader-white-bg-sm.gif`
- `/Images/loader-white-bg.gif`
- `/Images/loader-white-bg-x-sm.gif`

The loader on the nav bar next to the logo needs to have `/Images/loader-main-slm15.gif` replaced as it's an `<img src>` tag with no class. 

### Favourite Start
This is a sprite, class is called `.icon-favorite { }`.  Image that needs replaced is in `/Images/snow-ui-sprite.png`.

### Checkboxes
Checkboxes across the platform are actually icons, these are located in `Images/snow-ui-sprite.png`.

The class it uses is `.swui-checkbox`

## Snowboard
### Alert Dot
The alert 'dot' under the Alert List is an icon, this is located in `Images/snow-ui-sprite.png`.

The class it uses is `.alert-container .list .new .remark`, 

## Reports Page
### Report Icon
`icon-report-stock.png` needs replaced as the background is blue within the png, it's located here `Images/icon-report-stock.png`.

## DevExpress
Snow uses DevExpress for a lot of the components in the platform, the ones I've changed are at the bottom of `custom.css`.  It's hit or miss on whether these look any good, so if you want to remove them just remove everything after `/* Dev Express :: Start */`.

### .sw-Checkbox_Input:checked+.sw-Checkbox_Label:before
Snow (or DevExpress) decided to draw out a tick here in SVG, if you want to change the color if it you'll need to modify the base64 svg at the end of `custom.css`.  I've left a comment above it to explain what you need to do.  It defaults to greyish black at the moment.

