---
title: CloudWindow
layout: reference
---
struct simul::clouds::CloudWindow
===
void GetLatitudeLongitudeHeading(pos,lat,lon,head)
------

double GetOriginHeadingDegrees()
------

/< Get the latitude/longitude referred to by the specified quaternion.
void GetOriginLatitudeLongitudeHeading(lat,lon,head)
------

/< Get the latitude/longitude referred to by the specified position value.
void InitWindowCentre(lat_degrees,long_degrees,x_heading_degrees)
------

/ Initialize the window.
void MoveCloudWindow(x,y)
------

float UpdateWindowCentre(lat_degrees,long_degrees)
------

/ Returns updated x heading in degrees.
