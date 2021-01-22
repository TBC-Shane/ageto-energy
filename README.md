# ageto-energy
## Homepage Globe SOP
The globe illustration on the homepage of the Ageto Energy site is built completely in SVG. There are currently two files being loaded in:
* The globe itself: ageto_energy_globe_icon_white.svg, loaded into the page using Avada's Image Block
* The pins and their corresponding tooltips: globe_locations_pins.svg, loaded onto the page with Avada's Code Block. 

CSS is also required to enable the hover states of the various pins on the page. The CSS file can be accessed by going to the AGT_Ageto Energy folder on the Toolbox Creative Dropbox Server. Inside the file, navigate to _General_ > _AgetoWebsite_ and pull the file into CodeKit for processing. CSS for the Globe can be found in the layout.scss file.

The pins and tooltips are created using the following .eps file: GlobeIllustrationBlue_DEV.eps. The workflow for generating this file, and then modifying it for interaction is as follows:
1. Open GlobeIllustrationBlue_DEV.eps.
1. Duplicate one of the existing pins and rename it in the layers panel to the next location number in the string. For example, if there are 16 existing pins, rename your pin layer to _Location 17_. **The naming of each of the layers in this walkthrough is crucial to saving time and to maintaining an orderly and programmable file structure when output as an SVG file.**
1. Drag your pin into the appropriate location on the map.
1. Now, drag your new pin layer into the appropriate order in the layers panel. For example, we would drag this pin layer above the _Location 16_ pin layer.
1. On the far left of the file is the Tooltip template box. This box is editable and should be _duplicated only_ to generate new project information as needed.
1. Once duplicated, you can modify the text to the appropriate location information. 
1. Update the location information now.
1. Click into your text group until only the text is editable. Then, use **Command + Shift + O** to outline the type. With the type still selected, go to _Object > Compound Path > Make_. Recolor your letters as necessary. 
1. For your new tooltip layer, use the following naming convention: _Location # Project Information_, where _#_ is your current pin number. For this example, our layer would be named, _Location 17 Project Information_.
1. Position this layer next to its corresponding pin.
1. With your new tooltip layer named and positioned, we'll now be adding it to the pin layer group you created earlier. Open the Layers panel and select your tooltip layer. Now, drag it **into** the corresponding pin layer. When dragging a layer into another, you'll notice the layer highlights instead of showing a line above or below the layer. In this example, we'll be dragging the _Location 17 Project Information_ layer **into** the _Location 17_ layer.
1. Ensure all of your other layers follow this same naming convention and grouping.

## Exporting
1. Select the entire pins layer (all of our pins and their corresponding tooltips should be in this group) and drag it into the Asset Export panel.
1. Choose **SVG** under format.
1. Name the export _globe_locations_pins_date.svg_, where _date_ is the date of your export.
1. Click **Export**. Save the file to Dropbox: **/Active/AGT_Ageto Energy/20AGT0002-0004_Ageto Website Redesign Campaign/20AGT0004_Brand Implementation_Website Design and Front-End Development/Production Files/Comps/Art_Images/_website/illustrations/**. Illustrator will automatically save the new file under the SVG folder in this directory. 

### Resaving the export
1. Navigate to the file folder where you saved your new file. Open the SVG in Illustrator and then re-save the file into the same location. This will un-minify the file and will make it easier to edit. 

### Modify the SVG
1. Now open the file in the code editor of your choice.
1. **Shane to finish SOP here** (add `.project-information` class, add new Location class to CSS file, copy and paste SVG code to the website, etc.)
