/**
 * Get all the highway ways in Berlin Region.
 * Filter out bus stops and service highways.
 */
[out:json][timeout:400];
( area["admin_level"="4"]["wikidata"="Q64"]; )->.a;
(
    way["highway"]["name"]["highway"!="bus_stop"]["highway"!="elevator"]["highway"!="platform"]["highway"!="service"](area.a);
    way["place"="square"]["name"](area.a);
    way["leisure"="park"]["name"](area.a);
);
out body;
>;
out skel qt;