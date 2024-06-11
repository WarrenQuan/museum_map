# Museum Map Testing and Research 

Throughout testing, I researched two different methods of integrating Google Maps into a website to display a single location and neighborhood attractions with custom styles and markers. 

1. Embedded Link with Google My Maps (recommended for final implementation and simple future maintainability)
2. JS implementation of Google Maps with the [Maps JavaScript API](https://developers.google.com/maps/documentation/javascript).

## Embedded Links (Recommended)
[Google My Maps](https://www.google.com/maps/d/u/0/) allows users to create and share their own maps with custom markers through an accessible UI, which can then be shared to other users. By manually adding a location or importing a spreadsheet with addresses and details, users can quickly add locations. Limitations include a non-removable top-bar showing when embedded to webpage (without styling manipulation) and only nine different base map styles. An [example map](https://www.google.com/maps/d/u/0/edit?mid=1PEsvvV5_N5PIceTYL67phHOrUpzbjzM&usp=sharing) was made for this prototype. Refer to map_embedded.html and neighborhood_map_embedded.html for example HTML website.
![image](https://drive.google.com/uc?id=1VOOdSIpr7TB5XEGQTqzOy7ZeSk63PHfT)
*Prototype of My Neighborhood Embedded on Website (Without Topbar)*

## JS Implementation
Developers can also create their own Google Maps through code and the Maps Javscript API, which enables more customability. However, this complicates maintainability and requires more steps. To get started, an API key must be created through the Google Maps Platform Credentials page. [Refer to the following page for initial steps.](https://developers.google.com/maps/documentation/embed/quickstart#api-key).

Afterward, Google Maps allows for customizing and filtering what to show with the base map, opposed to the eight styles available for GoogleMyMaps. This can be manipulated through [JSON styling wizard Google provides](https://mapstyle.withgoogle.com/), [third party websites like Snazzy Maps](https://snazzymaps.com/explore), or [using the now recommended Cloud Console and linking a specific mapId](https://developers.google.com/maps/documentation/maps-static/cloud-customization). The file with the JS methods uses the recommended Cloud Console method following the documentation steps. 

Afterward, all markers has to be manually added through code in Longitude and Latitude. [Developers can add custom markers with editable sizes for each](https://developers.google.com/maps/documentation/javascript/custom-markers). If this method is developed further, the file and code should read from a CSV file or database for best maintainability practice, but the code currently stores the information through an array for initial prototype. [To make these markers interactable, additional title and content values are needed alongside an event listener (not implemented in current prototype).](https://developers.google.com/maps/documentation/javascript/advanced-markers/accessible-markers).

Although this allows for more customability and flexibility with how we want the map appears to users, the JS implementation is not recommended due to more difficult code maintability. Meanwhile, GoogleMyMaps can allow for all staff members to contribute their locations and allow for the map to update dynamically.


## Google Maps Link: Your Location to Brooklyn Museum
MoMA has a Get directions to MoMa link which goes from Your Location to MoMa. Similarly, this can be created for the Brooklyn Museum with the link: https://www.google.com/maps/dir/?api=1&destination=Brooklyn+Museum&destination_place_id=ChIJyTmcRApbwokR-oXJRqpVI8Y

- [api=1 specifies Maps URLs API is being used](https://developers.google.com/maps/documentation/urls/get-started)
- [destination=Brooklyn+Museum specifies a URL encoded version of the destination](https://developers.google.com/maps/documentation/urls/get-started#parameters)
- destination_place_id=ChIJyTmcRApbwokR-oXJRqpVI8Y, every location has a unique [place_id](https://developers.google.com/maps/documentation/places/web-service/place-id), a textual identifier that uniquely identifies a place, which ensures this map link routes to this exact location
