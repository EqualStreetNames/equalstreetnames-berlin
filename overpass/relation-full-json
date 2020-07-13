/**
 * Get all the relevant relations in Brussels Region.
 */
[out:json][timeout:300];
( area["admin_level"="4"]["wikidata"="Q64"]; )->.a;
(
    relation["type"="associatedStreet"]["name"](area.a);
);
out body;
>;
out skel qt;