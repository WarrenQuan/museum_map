# Museum Map Testing and Research 

Throughout testing, I researched two different methods of integrating Google Maps into a website to display a single location and neighborhood attractions with custom styles and markers. 

1. Embedded Link with Google My Maps (recommended for final implementation and simple future maintainability)
2. JS implementation of Google Maps with the [Maps JavaScript API](https://developers.google.com/maps/documentation/javascript).

## Embedded Links (Recommended)
[Google My Maps](https://www.google.com/maps/d/u/0/) allows users to create and share their own maps with custom markers through an accessible UI, which can then be shared with other users. By manually adding a location or importing a spreadsheet with addresses and details, users can quickly add locations. Limitations include a non-removable top bar showing when embedded in the webpage (without styling manipulation) and only nine different base map styles. An [example map](https://www.google.com/maps/d/u/0/edit?mid=1PEsvvV5_N5PIceTYL67phHOrUpzbjzM&usp=sharing) was made for this prototype. Refer to map_embedded.html and neighborhood_map_embedded.html for an example HTML website.
![image](https://drive.google.com/uc?id=1VOOdSIpr7TB5XEGQTqzOy7ZeSk63PHfT)
*Prototype of My Neighborhood Embedded on Website (Without Topbar)*

## JS Implementation
Developers can also create their own Google Maps through code and the Maps JavaScript API, which enables more customizability. However, this complicates maintainability and requires more steps. To get started, an API key must be created through the Google Maps Platform Credentials page. [Refer to the following page for initial steps.](https://developers.google.com/maps/documentation/embed/quickstart#api-key).

Afterward, Google Maps allows for customizing and filtering what to show with the base map, opposed to the eight styles available for GoogleMyMaps. This can be manipulated through [JSON styling wizard Google provides](https://mapstyle.withgoogle.com/), [third party websites like Snazzy Maps](https://snazzymaps.com/explore), or [using the now recommended Cloud Console and linking a specific mapId](https://developers.google.com/maps/documentation/maps-static/cloud-customization). The file with the JS methods uses the recommended Cloud Console method following the documentation steps. 

Afterward, all markers have to be manually added through code in Longitude and Latitude. [Developers can add custom markers with editable sizes for each](https://developers.google.com/maps/documentation/javascript/custom-markers). If this method is developed further, the file and code should read from a CSV file or database for best maintainability practice, but the code currently stores the information through an array for the initial prototype. [To make these markers interactable, additional title and content values are needed alongside an event listener (not implemented in current prototype).](https://developers.google.com/maps/documentation/javascript/advanced-markers/accessible-markers).

Although this allows for more customizability and flexibility with how we want the map to appear to users, the JS implementation is not recommended due to more difficult code maintainability. Meanwhile, GoogleMyMaps can allow for all staff members to contribute their locations and allow for the map to update dynamically.

![image](https://drive.google.com/uc?id=18qv1d_PIj7yDi4rLzVvJpmVTB1GPMOtx)
*Prototype of My Neighborhood Using JS*

## Google Maps Link: Your Location to Brooklyn Museum
MoMA has a Get directions to MoMa link which goes from [Your Location to MoMa](https://www.google.com/maps/dir/?api=1&destination=MoMA&destination_place_id=ChIJKxDbe_lYwokRVf__s8CPn-o). Similarly, this can be created for the Brooklyn Museum with the link: https://www.google.com/maps/dir/?api=1&destination=Brooklyn+Museum&destination_place_id=ChIJyTmcRApbwokR-oXJRqpVI8Y. This should be added to the "Get Directions" button.

- [api=1 specifies Maps URLs API is being used](https://developers.google.com/maps/documentation/urls/get-started)
- [destination=Brooklyn+Museum specifies a URL encoded version of the destination](https://developers.google.com/maps/documentation/urls/get-started#parameters)
- destination_place_id=ChIJyTmcRApbwokR-oXJRqpVI8Y, every location has a unique [place_id](https://developers.google.com/maps/documentation/places/web-service/place-id), a textual identifier that uniquely identifies a place, which ensures this map link routes to this exact location

## Benchmarking
Competitor analysis was done in comparison to museums locally in New York City in the Museums Council of New York (50+ Museums) alongside a handful of selected museums nationwide and international museums. Museums are sorted into three different categories and the focus should be on Custom Map Graphics. Prior research has been done on MoMa with its link to Google Maps. 
  
### Custom Map Graphics
- [American Academy of Arts and Letters](https://www.artsandletters.org/visit): Can click on map graphic for Google Map link of museum
- [Discovery Maps](https://discoverymap.com/princeton-nj): Uses Mapbox for custom graphic map
- [Dyckman Farmhouse Museum](https://dyckmanfarmhouse.org/visit/hours-directions/): Mapbox + Google Maps
- [Fraunces Tavern® Museum](https://www.frauncestavernmuseum.org/admissions): Stylized Google Maps
- [Gateway National Recreation Area](https://www.nps.gov/gate/planyourvisit/maps.htm): Stylized MapBox
- [Ghibli Museum](https://ghibli-park.jp/en/directions/): Hand-drawn graphic + Google Maps embedded at bottom
- [Intrepid Museum](https://intrepidmuseum.org/plan-your-visit/visitor-information)
- [Morris-Jumel Mansion](https://morrisjumel.org/visit/)
- [Museum at Eldridge Street](https://www.eldridgestreet.org/visit)
- [National Palace Museum](https://www.npm.gov.tw/Articles.aspx?sno=03009216&l=2): Graphic detailing all possible bus routes accompanied with text
- [Solomon R. Guggenheim Museum](https://www.guggenheim.org/plan-your-visit/ideas-for-your-visit)
    - Includes small graphic of map with the location and link to the Guggenheim Museum when clicked *Get Directions*
    - Neighborhood section includes text recommendations with links to articles and apps (like Bloomberg Connect and NYC Tourism webpage) on activities, no visual guide**
- [The Art Institute of Chicago](https://www.artic.edu/visit)
- [The Drawing Center](https://drawingcenter.org/visit): Stylized Google Maps

### Embedded Google Maps
- [AS/COA New York | Americas Society/Council of the Americas](https://www.as-coa.org/art)
- [Bayside Historical Society](https://www.baysidehistorical.org/visit-us)
- [British Museum](https://www.britishmuseum.org/visit#getting-here)
- [Bronx Museum](https://bronxmuseum.org/visit/)
- [Cooper-Hewitt](https://www.cooperhewitt.org/visit/getting-here/)
- [Dahesh Museum of Art](https://www.daheshmuseum.org/visit/)
- [De Young Museum](https://www.famsf.org/visit/getting-to-the-de-young)
- [Greenwood Museum](https://www.green-wood.com/visit/)
- [The Grolier Club](https://www.grolierclub.org/Default.aspx?p=DynamicModule&pageid=384820&ssid=322441&vnf=1)
- [Harbor Defense Museum](https://history.army.mil/museums/IMCOM/fortHamilton/index.html#visit)
- [Hispanic Society Museum & Library](https://hispanicsociety.org/visit/visitor-information/)
- [International Center of Photography](https://www.icp.org/visit)
- [Japan Society Gallery](https://japansociety.org/about/visit-us/)
- [Tenement Museum](https://www.tenement.org/plan-a-visit/)
- [MoMa PS1](https://www.momaps1.org/visit)
- [Museum of the City of New York](https://www.mcny.org/visit)
- [Museum at the Fashion Institute of Technology](https://www.fitnyc.edu/museum/visit/index.php)
- [Museum of Food and Drink in Brooklyn](https://www.mofad.org/location)
- [Vatican Museums](https://www.museivaticani.va/content/museivaticani/en/info/come-raggiungerci.html)

### Text Descriptions
- [Alice Austen House Museum](https://aliceausten.org/planyourvisit/)
- [Alley Pond Environmental Center](https://www.alleypond.org/your-visit.html): does link to PDF [park map](https://www.alleypond.org/uploads/1/2/8/3/128396335/alley-pond-park-trail-guide__57d311db0b919_1.pdf) for walking
- [American Folk Art Museum](https://folkartmuseum.org/news/visitor-guidelines/)
- [American Museum of Natural History](https://www.amnh.org/plan-your-visit)
- [American Numismatic Society](https://www.google.com/search?q=the+american+numismatic+society+visit&sca_esv=ee550f040f73c7f6&sca_upv=1&sxsrf=ADLYWIKi_GZmPorZDh_0SZyOPvjYGcnOzA%3A1718130527241&ei=X5doZvy4Du2hptQPs8SKqAQ&ved=0ahUKEwi85IP-ltSGAxXtkIkEHTOiAkUQ4dUDCBA&uact=5&oq=the+american+numismatic+society+visit&gs_lp=Egxnd3Mtd2l6LXNlcnAiJXRoZSBhbWVyaWNhbiBudW1pc21hdGljIHNvY2lldHkgdmlzaXQyBRAhGKABMgUQIRigATIFECEYoAEyBRAhGKABSLMGUERYrwVwAXgBkAEAmAF7oAGdBKoBAzQuMrgBA8gBAPgBAZgCB6ACrwTCAgoQABiwAxjWBBhHwgINEAAYsAMY1gQYRxjJA8ICDhAAGIAEGLADGJIDGIoFwgIFEAAYgATCAgYQABgWGB7CAgsQABiABBiGAxiKBcICCBAAGIAEGKIEwgIFECEYqwLCAgUQIRifBZgDAIgGAZAGCZIHAzUuMqAH5CA&sclient=gws-wiz-serp)
- [Asia Society Museum](https://asiasociety.org/new-york/plan-your-visit)
- [Botanical Garden](https://www.nybg.org/visit/): has garden map
- [Brooklyn Children’s Museum](https://www.brooklynkids.org/visit/)
- [Center for Jewish History](https://www.cjh.org/visit/plan-your-visit)
- [El Museo del Barrio](https://www.elmuseo.org/plan-your-visit/)
- [The Frick Collection](https://www.frick.org/visit)
- [The Jewish Museum](https://thejewishmuseum.org/visit)
- [Merchant’s House Museum](https://merchantshouse.org/visit/)
- [MET](https://www.metmuseum.org/plan-your-visit)
- [Morgan Library & Museum](https://www.themorgan.org/visit)
- [Mount Vernon Hotel Museum & Garden](https://mvhm.org/visit/)
- [Museum of Arts and Design](https://madmuseum.org/visit)
- [Museum of Chinese in America](https://www.mocanyc.org/visit/museum-virtual-tour/)
