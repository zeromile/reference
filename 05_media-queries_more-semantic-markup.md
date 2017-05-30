# 05 - media queries, more semantic markup #

Continue with Bootstrap pet-store site

RWD - The Viewport (http://w3schools.com/css/css_rwd_viewport.asp)
- The viewport is the visible area of a web page
- Each device has a different viewport and desktop browsers can be varied because the user can resize the browser window
- The <meta> tag should always contain a viewport designation
    - <meta name=“viewport” content=“width=device-width, initial-scale=1.0”>
    - width=device-width sets the width of the page to follow the screen-width of the device
    - initial-scale=1.0 sets the initial zoom of the page
    - try rebuilding the view with and without example on the w3schools page
- Always use relative value widths, not fixed. Even though a media query can change css if the screen size change…if you your widths are fixed your layout could still be off the page

GRID VIEW (http://www.w3schools.com/css/css_rwd_grid.asp)
- Build a page using the grid view
- selectors in square brackets are called attribute selectors (http://w3schools.com/css/css_attribute_selectors.asp)
    - It’s like a matching thing - “if there is an element that has an attribute that matches this then do this style…”
    - [title~=“flower”] will match elements with title="flower", title="summer flower", and title="flower new", but not title="my-flower" or title="flowers".
    - continue working through RWD grid view

Media Queries (http://w3schools.com/css/css_rwd_mediaqueries.asp)
- A media query is a CSS module that allows content rendering to adapt to conditions such as screen resolution 
- A media query consists of a media type and one or more expressions, involving media features, which resolves to either true or false
- Media types (display devices)
    - braille
    - embossed
    - handheld
    - print
    - projection
    - screen
    - speech
    - tty
    - TV
    - all
- Media features (attributes of the display devices)
    - color (#bits)
    - device-height
    - device-width
    - resolution
    - height
    - width
    - 
