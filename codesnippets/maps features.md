# maps features
maps notes:
* Open Street is good for streets, cities, but not home addresses - Nominatim is better used for that (this seems to be slightly less accurate compared to Google’s reverse geocoding)
* Use coords to get accurate street address through reverse geocoding (Google Maps, Open Street’s Nominatim like MapQuest)
	* Then
		* use a pattern to get addresses on that street while verifying them
			* either several in both directions (requires algorithm to detect block jumps in house numbering)
			* or based on an address range ( [https://www2.census.gov/geo/pdfs/maps-data/data/tiger/tgrshp2013/TGRSHP2013_TechDoc_Ch6.pdf](https://www2.census.gov/geo/pdfs/maps-data/data/tiger/tgrshp2013/TGRSHP2013_TechDoc_Ch6.pdf) ) (if this had coords then verification may be only necessary upon shipping?)
		* or use an api to reverse geocode an area
* Or use coords to get the street name
	* Then
		* use an api to gather start and end address numbers (address range) (where? TIGER is okay)
		* use an api to get street numbers on street (where?)
* Use a service like [here.com](http://here.com)
	* [https://developer.here.com/rest-apis/documentation/geocoder/topics/examples-reverse-geocoding.html](https://developer.here.com/rest-apis/documentation/geocoder/topics/examples-reverse-geocoding.html)
	* [http://gis.stackexchange.com/questions/116437/how-to-get-lat-long-of-all-adresses-inside-a-polygon-in-google-map](http://gis.stackexchange.com/questions/116437/how-to-get-lat-long-of-all-adresses-inside-a-polygon-in-google-map)
	* here turned out to be neat for proximity / radius, but returned very incomplete results

[http://nominatim.openstreetmap.org/reverse?format=xml&lat=42.9763865&lon=-85.6623379&zoom=18&addressdetails=1](http://nominatim.openstreetmap.org/reverse?format=xml&amp;lat=42.9763865&amp;lon=-85.6623379&amp;zoom=18&amp;addressdetails=1)
[https://maps.googleapis.com/maps/api/geocode/json?latlng=42.9763865,-85.6623379&key=AIzaSyCqFW9Pq_sJ8bNBx8f9gzS_1mHw7_H_5iI](https://maps.googleapis.com/maps/api/geocode/json?latlng=42.9763865,-85.6623379&amp;key=AIzaSyCqFW9Pq_sJ8bNBx8f9gzS_1mHw7_H_5iI)

[https://www.mapbox.com/api-documentation/#request-format](https://www.mapbox.com/api-documentation/#request-format)
[http://results.openaddresses.io/](http://results.openaddresses.io/) incomplete for MI
[http://www.whitepages.com/neighbors/f1fe043c-736e-4cb5-8b05-799618ab1b8e](http://www.whitepages.com/neighbors/f1fe043c-736e-4cb5-8b05-799618ab1b8e) not available via API, crawl?

the plan:
* Use current location to find nearest street address
	* if an exact address like 733 cannot be found - how to get address range? TIGER off the bat?
* Then “guess” and verify 10 address back and 10 address forward (the range)
	* May cost upwards of 40, 100 requests
	* Intelligently detect block jumps (780 to 801)? (space is not always a block jump)
	* Is “guess”ing with coords less requests than each number possibility?
* Limit # of verification requests by
	* doing requests at regular interval
	* and when moving / driving at slow speed
	* and when no longer in range that’s already verified
	* **bulk verification?**
	* don’t display dots until clicking on home? (color codes work thereafter)
* Later: integrate TIGER database which is said to include address ranges
	* this will improve the “guess”
	* also helps detect block-jumps
* Later: build caching mechanism to store verified data on our server
* Later: find and consider an address database

Nope, forget the grey dots.

#department/development/codesnippets