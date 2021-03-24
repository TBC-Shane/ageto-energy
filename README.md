# ageto-energy
## Sketch Homepage Globe SOP
The globe illustration on the homepage of the Ageto Energy site is built completely in SVG. There are currently two files being loaded in:
* The globe itself: ageto_energy_globe_icon_white.svg, loaded into the page using Avada's Image Block
* The pins and their corresponding tooltips: globe_locations_pins.svg, loaded onto the page with Avada's Code Block. 

CSS is also required to enable the hover states of the various pins on the page. Update Toolbox Creative (hosting@toolboxcreative.com) should the map exceed 50 locations.

The pins and tooltips are created using the following .eps file: GlobeIllustrationBlue_DEV.svg. The workflow for generating this file, and then modifying it for interaction is as follows:
1. Open GlobeIllustrationBlue_DEV using Sketch. If you do not own a copy of the Sketch application, you can purchase it [here.](https://www.sketch.com/)
2. Down the left-hand side of the application you will find a list of layers. Spin down the "pins" layer and then spin down the Pin Icons layer.  
3. Duplicate one of the existing pin layers by right-clicking on the layer name (e.g. _Location_24_) and selecting Duplicate. Rename it in the layers panel to the next location number in the string. For example, if there are 24 existing pins, rename your pin layer to _Location 25_. **The naming of each of the layers in this walkthrough is crucial to saving time and to maintaining an orderly and programmable file structure when output as an SVG file.**
4. Twirl down the layer and select the pin "Path" object to view the location of your new pin on the map. Drag your pin into the appropriate location on the map.
5. Now, drag your new pin layer into the appropriate order in the layers panel. For pins with tooltips to their right, it works best to have locations further to the left on the map higher in the layers. This ensures that the rollover state goes over any pins to the right and reduces the chances for map pins displaying on top of other map meta data. Taking the time now to ensure that your layer is in the proper order will save time in the future.
6. Back in the layers panel, select the project information layer folder (i.e. _Location_25_Project_Information_).
10. Rename this folder usinh the following naming convention: _Location_#_Project Information_, where _#_ is your current pin number. For this example, our new layer would be named, _Location_25_Project_Information_.
11. Position this layer next to its corresponding pin. Ensure that this layer does not overlap the pin in any way. That way, pin interaction will not be interrupted by a tooltip pop-up.
12. Modify the text in the Location Name, Project Type and State, Country text boxes in your new group. Simply double-click on the text you'd like to modify in the canvas.
13. If you are adding multiple locations, ensure all of your other layers follow this naming convention and grouping.

## Exporting
1. Make sure each layer in your Sketch document is visible. Any layers left hidden will not be exported to the SVG. To toggle visibility on a layer, hover over the layer in the layers panel and click the eye icon to the right of the layer name.
2. Go to **File > Export**. Click **Export.**
3. Name the export _globe_locations_date.svg_, where _date_ is the date of your export (e.g. _globe_locations_03-24-21.svg_).
4. Click **Save**. Save the file to your corresponding folder on your server or desktop.

### Modify the SVG to add CSS Class
1. Now open the file in the code editor of your choice. We recommend the free [Visual Studio Code](https://code.visualstudio.com/) if you don't already have a preference.
1. To set up the hover state of each tootlip, we'll need to include a class on each project information panel. To do this, we can perform a search and replace for the end of the project information `id` that Sketch creates for us. For example, I search for `_Information"` and then replace it with `_Information" class="project-information"`. This adds the `project-information` class to each project information tooltip panel in the file. 
2. In Visual Studio, open your _globe_locations_date.svg_ file, then go to **Edit > Replace**. In the top search box enter `_Information"` and in the bottom replace box enter `_Information" class="project-information"`. On Mac, click **Command + Enter** on your keyboard to replace all (Click **ctrl + Enter on PC**). Alternatively you can click the second icon to the right of the replace box.  
3. Now save the file. Keep this file open, we'll use it in a moment.


## Preparing the website
### Adding the SVG code
1. Navigate to the homepage and edit the page. Scroll down to the Code Block in the **100% Satisfied** section. Copy the SVG code from your code editor and paste the SVG code **in-between** the `<div>` tags. The structure should be as follows:
`<div class="globe-pins">`
`your new svg code`
`</div>`


## Creating the mobile version of the file
1. Open the most recent version of the **ageto_energy_globe_mobile_updated** Sketch file. 
1. Using the layers panel on the left side of Sketch, select and existing pin and right-click on it. Choose duplicate and then move the new pin to its corresponding new location on the map. Save the file. 
2. Go to **File > Export.** Click **Export**. Rename the file to append today's date, like so: **ageto_energy_globe_mobile_updated_03-24-21.svg** and save to its corresponding folder.

### Adding the mobile view
1. In the 1/1 container directly below the Code Block you just modified, upload the new mobile svg image file you created. *No need to copy and paste the SVG here, as this will only be an image*. Save the image container.

### Finishing up
1. Preview the changes you have made to the homepage to ensure your new svg code is displaying as intended. 
1. Be sure to check mobile sizes for your new mobile map image as well. 
1. Debug any strange overlaps, etc. by reordering the layers in your svg file to suit the new map. 
1. Click **Update**. 
1. Clear any caches on the site. 

## Additional Resources
1. Ageto Energy location map (updated 02-04-21): https://www.google.com/maps/d/u/0/edit?mid=1kyaZQfb_zhICuGYE9hdB9tVA75mjnfd8&usp=sharing
