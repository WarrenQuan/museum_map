# Museum Map Testing and Research 

Throughout testing, I researched two different methods of integrating Google Maps into a website to display a single location and neighborhood attractions with custom styles and markers. 

1. Embedded Link with Google My Maps (recommended for final implementation and simple future maintainability)
2. JS implementation of Google Maps with the [Maps JavaScript API](https://developers.google.com/maps/documentation/javascript).

## Embedded Links (Recommended)
[Google My Maps](https://www.google.com/maps/d/u/0/) allows users to create and share their own maps with custom markers through an accessible UI, which can then be shared to other users. By manually adding a location or importing a spreadsheet with addresses and details, users can quickly add locations. Limitations include a non-removable top-bar showing when embedded to webpage (without styling manipulation) and only nine different base map styles. An [example map](https://www.google.com/maps/d/u/0/edit?mid=1PEsvvV5_N5PIceTYL67phHOrUpzbjzM&usp=sharing) was made for this prototype. Refer to map_embedded.html and neighborhood_map_embedded.html for example HTML website.
![image](https://drive.google.com/uc?id=1VOOdSIpr7TB5XEGQTqzOy7ZeSk63PHfT)
*Prototype of My Neighborhood Embedded on Website (Without Topbar)*

## JS Implementation
Write Later

## Google Maps Link: Your Location to Brooklyn Museum
MoMA has a Get directions to MoMa link which goes from Your Location to MoMa. Similarly, this can be created for the Brooklyn Museum with the link: https://www.google.com/maps/dir/?api=1&destination=Brooklyn+Museum&destination_place_id=ChIJyTmcRApbwokR-oXJRqpVI8Y

- [api=1 specifies Maps URLs API is being used](https://developers.google.com/maps/documentation/urls/get-started)
- [destination=Brooklyn+Museum specifies a URL encoded version of the destination](https://developers.google.com/maps/documentation/urls/get-started#parameters)
- destination_place_id=ChIJyTmcRApbwokR-oXJRqpVI8Y, every location has a unique [place_id](https://developers.google.com/maps/documentation/places/web-service/place-id), a textual identifier that uniquely identifies a place, which ensures this map link routes to this exact location
