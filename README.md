# ageto-energy
## Homepage Globe SOP
The globe illustration on the homepage of the Ageto Energy site is built completely in SVG. There are currently two files being loaded in:
* The globe itself: ageto_energy_globe_icon_white.svg, loaded into the page using Avada's Image Block
* The pins and their corresponding tooltips: globe_locations_pins.svg, loaded onto the page with Avada's Code Block. 

CSS is also required to enable the hover states of the various pins on the page. The CSS file can be accessed by going to the AGT_Ageto Energy folder on the Toolbox Creative Dropbox Server. Inside the file, navigate to _General_ > _AgetoWebsite_ and pull the file into CodeKit for processing. CSS for the Globe can be found in the layout.scss file.

The pins and tooltips are created using the following .eps file: GlobeIllustrationBlue_DEV.eps. The workflow for generating this file, and then modifying it for interaction is as follows:
1. Open GlobeIllustrationBlue_DEV.eps.
1. Duplicate one of the existing pins and rename it in the layers panel to the next location number in the string. For example, if there are 16 existing pins, rename your pin layer to _Location 25_. **The naming of each of the layers in this walkthrough is crucial to saving time and to maintaining an orderly and programmable file structure when output as an SVG file.**
1. Drag your pin into the appropriate location on the map.
1. Now, drag your new pin layer into the appropriate order in the layers panel. For pins with tooltips to their right, it works best to have locations further to the left on the map higher in the layers. This ensures that the rollover state goes over any pins to the right and reduces the chances for map pins displaying on top of other map meta data. Taking the time now to ensure that your layer is in the proper order will save time in the future.
1. On the far left of the file is the Tooltip template box. This box is editable and should be _duplicated only_ to generate new project information as needed.
1. Once duplicated, you can modify the text to the appropriate location information. 
1. Update the location information now.
1. Click into your text group until only the text is editable. Then, use **Command + Shift + O** to outline the type. With the type still selected, go to _Object > Compound Path > Make_. Recolor your letters as necessary. 
1. For your new tooltip layer, use the following naming convention: _Location # Project Information_, where _#_ is your current pin number. For this example, our layer would be named, _Location 25 Project Information_.
1. Position this layer next to its corresponding pin.
1. With your new tooltip layer named and positioned, we'll now be adding it to the pin layer group you created earlier. Open the Layers panel and select your tooltip layer. Now, drag it **into** the corresponding pin layer. When dragging a layer into another, you'll notice the layer highlights instead of showing a line above or below the layer. In this example, we'll be dragging the _Location 25 Project Information_ layer **into** the _Location 25_ layer.
1. Ensure all of your other layers follow this same naming convention and grouping.

## Creating the mobile version of the file
1. Open the most recent version of the **ageto_energy_globe_mobile_updated.svg** file. 
1. Rename the file to append today's date, like so: **ageto_energy_globe_mobile_updated_02-05-21.svg**.
1. Add a new pin that corresponds to your new location. Save the file back to **/Active/AGT_Ageto Energy/20AGT0002-0004_Ageto Website Redesign Campaign/20AGT0004_Brand Implementation_Website Design and Front-End Development/Production Files/Comps/Art_Images/_website/illustrations/SVG/**. 

## Exporting
1. Select the entire pins layer (all of our pins and their corresponding tooltips should be in this group as well as the surrounding transparent rectangle) and drag it into the Asset Export panel.
1. Choose **SVG** under format.
1. Name the export _globe_locations_pins_date.svg_, where _date_ is the date of your export.
1. Click **Export**. Save the file to Dropbox: **/Active/AGT_Ageto Energy/20AGT0002-0004_Ageto Website Redesign Campaign/20AGT0004_Brand Implementation_Website Design and Front-End Development/Production Files/Comps/Art_Images/_website/illustrations/**. Illustrator will automatically save the new file under the SVG folder in this directory. 

### Resaving the export
1. Navigate to the file folder where you saved your new file. Open the SVG in Illustrator and then re-save the file into the same location. This will un-minify the file and will make it easier to edit. 

### Modify the SVG
1. Now open the file in the code editor of your choice.
1. To set up the hover state of each tootlip, we'll need to include a class on each project information panel. To do this, I perform a search and replace for the end of the project information `id` that illustrator creates for us. For example, I search for `_Information"` and then replace it with `_Information" class="project-information"`. This adds the `project-information` class to each project information tooltip panel in the file. Now save the file. Keep this file open, we'll use it in a moment.


## Preparing the website
### Adding our CSS
1. We'll need to add a new css rule to correspond to our new location. Open the **/_AgetoWebsite_** folder in your preferred code editor, making sure **CodeKit** is open and running to compile the file. Navigate to the `layout.css` file. Do a search for `Homepage Globe` to find the corresponding section. We'll be focusing on the Location listings (`&#Location_24:hover`). 
1. Add your new location to the end of the list. For our example, we would add a `,` after the last listing and add `&#Location_25:hover` to the end. Save the file. 
1. Upon save, you should get a successful Compiled notification from CodeKit. Navigate to the main-min.css folder and copy the code. 
1. Open the Ageto website and login. Go to the Avada Options panel (`Avada > Options`) and scroll down to the Custom CSS section. Paste your CSS here and Save the panel. 
### Adding the SVG code
1. Navigate to the homepage and edit the page. Scroll down to the Code Block underneath the empty globe image in the **100% Satisfied** section. Copy the SVG code from your code editor and paste the SVG code **in-between** the `<div>` tags. The structure should be as follows:
`<div class="globe-pins">`
`your new svg code`
`</div>`
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
