# Flash Cards
Simple, animated, and imageless flash cards using HTML/CSS/jQuery.

## Features
 
* Easily tweaked appearance <small>(requires [SASS](http://sass-lang.com)/[Compass](http://compass-style.org) or old-fashioned overrides)</small>  
<small>Simply edit variables in [_flash_cards.scss](/curtisblackwell/flash_cards/blob/master/css/_flash_cards.scss) to update dimensions and colors.</small>
* Simple markup  
<small>The deck is a list and the cards are list items with a div for each side.</small>
* No images  
<small>Cards are 100% CSS, and buttons are an icon font consisting only of the icons used.</small>

## Dependencies
* jQuery
* [jQuery Cycle](http://jquery.malsup.com/cycle)
* [Modernizr](http://modernizr.com) (<small>If you want the 3D transforms fallback</small>)

## Browser Support
This has been tested only in Chrome <small>(21.0.1155.2 dev)</small> and Firefox <small>(12.0)</small>.

I plan to support all major browsers, but I haven't had the need yet.

## Setup & Usage
1. ### Put the files in place.  

   <table>
     <thead>
       <th>Files</th>
       <th>Location</th>
     </thead>
     <tbody>
       <tr>
         <td>
           <b>If you're using <a href="http://sass-lang.com/">SASS</a>/<a href="http://compass-style.org/">Compass</a>:</b><br>
           <code>_flash_cards.scss</code> and <code>_fonts.scss</code><br>
           <b>If you're not using SASS/Compass:</b><br>
           <code>style.css</code>
         </td>
         <td>
           <br>
           Your SASS directory<br><br>
           Your CSS directory
         </td>
       </tr>
       <tr>
         <td>The contents of the <code>js</code> folder</td>
         <td>Your javascript directory</td>
       </tr>
       <tr>
         <td><code>resources</code></td>
         <td>Your root</td>
       </tr>
     </tbody>
   </table>

2. ### Include necessary code.  
   #### .css
   If you're SASSin' and Compassin' it up, `@import "flash_cards";` into your `.scss`. If not, use `style.css`.

   #### .js (and font)
   Place the following in your `<head>`:
   
        <link href="http://fonts.googleapis.com/css?family=Schoolbell" rel="stylesheet" type="text/css">
        <script src="path/to/modernizr-2.5.3.min.js"></script>

   and the following before `</body>`:

        <script src="path/to/flash_cards.min.js"></script>

3. ### The Markup
   #### The Deck
   The deck is a list with an id of deck. Each card is a list item containing a div for each side, 
   each div contains a paragraph.

        <ul id="deck">
          <li class="card">

            <div class="side_one">
              <p>How many licks does it take to get to the center of a Tootsie Pop?</p>
            </div>

            <div class="side_two">
              <p>The world may never know.</p>
            </div>

          </li>
        </ul>

   #### The Navigation
   The navigation uses an icon font put together using [IcoMoon](http://keyamoon.com/icomoon/app/), 
   so it contains only the necessary characters to keep file size down. 
   
   The markup follows Jon Hicks' [data-icon method](http://24ways.org/2011/displaying-icons-with-fonts-and-data-attributes).   
   
        <div id="nav_deck">
          <span class="icon" id="prev" data-icon="<"><span class="visuallyhidden">Previous</span></span>
          <span class="icon" id="flipper" data-icon="/"><span class="visuallyhidden">Flip</span></span>
          <span class="icon" id="next" data-icon=">"><span class="visuallyhidden">Next</span></span>
        </div>
   
   #### The Keyboard Shortcuts
   I created a table to display the available keyboard shortcuts, accessible via clicking an element with an id of icon 
   or hitting the forward-slash/question mark key.

        <div id="keyboard_shortcuts">
          <h1>Keyboard Shortcuts</h1>
          <table>
            <tbody>
              <tr>
                <td>Previous Card</td>
                <td>&larr;</td>
              </tr>
              <tr>
                <td>Next Card</td>
                <td>&rarr;</td>
              </tr>
              <tr>
                <td>Flip Card</td>
                <td>&uarr; <span class="or">/</span> &darr; <span class="or">/</span> Return <span class="or">/</span> Space</td>
              </tr>
              <tr>
                <td>Show/Hide Keyboard Shortcuts</td>
                <td>?</td>
              </tr>
            </tbody>
          </table>
        </div>

        <div class="icon" id="keyboard_shortcuts_toggle" data-icon="k"><span class="visuallyhidden">Keyboard Shortcuts</span></div>

## Icons not displaying properly?
Check the paths to the font files in `_fonts.scss` or `style.css`.

## License
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="http://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Flash Cards</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://curtisblackwell.github.io/flash_cards/" property="cc:attributionName" rel="cc:attributionURL">Curtis Blackwell</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
