---
title: Discovery Platform for Geospatial (GIS) Data
author: Anthony Jones
layout: post
thumbnail_url: http://appmango.net/anthonyjones/wp-content/uploads/2015/09/virgo-gis.jpg
project_image: http://appmango.net/anthonyjones/wp-content/uploads/2015/09/mobile-home-sized.jpg
subtitle: Designing a University of Virginia initiative to preserve & provide access to geospatial datalines.
category: Design
caption: image courtesy of Elizabeth Lies via unsplash.com
excerpt: In higher education, the discovery of GIS data is overly complicated and incomplete. We needed an application which enables the discovery of GIS data with an emphasis on user experience, integrates seamlessly with other tools, and streamlines the organization of geospatial data.
---

<div class="flow-text" itemprop="articleBody">
<p>In higher education, the discovery of GIS data is overly complicated and incomplete. We needed an application which enables the discovery of GIS data with an emphasis on user experience, integrates seamlessly with other tools, and streamlines the organization of geospatial data. </p>
<p>We decided to build this system using Geoblacklight. Geoblacklight is a Solr-powered discovery platform. We are also using OpenGeoportal, which is an open source federated metadata sharing community.</p>
<p>We are currently gathering more requirements and user testing. For now, the application only features the following: spatial search, text search, results text view, faceted search(possibly in the future). </p>
<p>Users should be able to save bookmarks, view history, and download Shapefiles. Today, I am sharing my first design iteration based on the few requirements that we have so far.</p>
<h4 class="light grey-text text-darken-1">Home Screen</h4>
<aside class="aside-left hide-on-med-and-down"><i>I plan on adding tutorial popups to the home screen for learning special features of the map and keyboard shortcuts.</i></aside>
<p><div class="material-placeholder"><img src="http://appmango.net/anthonyjones/wp-content/uploads/2015/09/home.jpg" alt="Home Screen for Virgo GIS" width="1200" height="1000" class="materialboxed radius-three responsive-img aligncenter size-full wp-image-1479 intialized" srcset="http://appmango.net/anthonyjones/wp-content/uploads/2015/09/home-300x250.jpg 300w, http://appmango.net/anthonyjones/wp-content/uploads/2015/09/home.jpg 1200w" sizes="(max-width: 1200px) 100vw, 1200px"></div></p>
<div class="image-caption center-align hide-on-large-only">I plan on adding tutorial popups to the home screen for learning special features of the map and keyboard shortcuts.</div>
<aside class="aside-left hide-on-med-and-down"><i>Responsive screens for mobile with slide-out drawer navigation</i></aside>
<p><div class="material-placeholder"><img src="http://appmango.net/anthonyjones/wp-content/uploads/2015/09/mobile-home-screens.jpg" alt="Virgo GIS Mobile Home Screens" width="1200" height="1000" class="materialboxed radius-three responsive-img aligncenter size-full wp-image-1483 intialized" srcset="http://appmango.net/anthonyjones/wp-content/uploads/2015/09/mobile-home-screens-300x250.jpg 300w, http://appmango.net/anthonyjones/wp-content/uploads/2015/09/mobile-home-screens.jpg 1200w" sizes="(max-width: 1200px) 100vw, 1200px"></div></p>
<div class="image-caption center-align hide-on-large-only">Responsive screens for mobile with slide-out drawer navigation</div>
<h4 class="light grey-text text-darken-1">Results Screens</h4>
<aside class="aside-left hide-on-med-and-down"><i>The results screen shows when moving the map(optional) or via text search</i></aside>
<p><div class="material-placeholder"><img src="http://appmango.net/anthonyjones/wp-content/uploads/2015/09/results.jpg" alt="Results Screen for Virgo GIS" width="1200" height="1000" class="materialboxed radius-three responsive-img aligncenter size-full wp-image-1476 intialized" srcset="http://appmango.net/anthonyjones/wp-content/uploads/2015/09/results-300x250.jpg 300w, http://appmango.net/anthonyjones/wp-content/uploads/2015/09/results.jpg 1200w" sizes="(max-width: 1200px) 100vw, 1200px"></div></p>
<div class="image-caption center-align hide-on-large-only">The results screen shows when moving the map(optional) or via text search</div>
<aside class="aside-left hide-on-med-and-down"><i>Individual record search result. The priority task is downloading the Shapefile.</i></aside>
<p><div class="material-placeholder"><img src="http://appmango.net/anthonyjones/wp-content/uploads/2015/09/record.jpg" alt="Individual Record Screen" width="1200" height="1000" class="materialboxed radius-three responsive-img aligncenter size-full wp-image-1478 intialized" srcset="http://appmango.net/anthonyjones/wp-content/uploads/2015/09/record-300x250.jpg 300w, http://appmango.net/anthonyjones/wp-content/uploads/2015/09/record.jpg 1200w" sizes="(max-width: 1200px) 100vw, 1200px"></div></p>
<div class="image-caption center-align hide-on-large-only">Individual record search result. The priority task is downloading the Shapefile.</div>
<aside class="aside-left hide-on-med-and-down"><i>Mobile results screen for responsive design</i></aside>
<p><div class="material-placeholder"><img src="http://appmango.net/anthonyjones/wp-content/uploads/2015/09/results-screens.jpg" alt="Mobile Results Screens" width="1200" height="1000" class="materialboxed radius-three responsive-img aligncenter size-full wp-image-1482 intialized" srcset="http://appmango.net/anthonyjones/wp-content/uploads/2015/09/results-screens-300x250.jpg 300w, http://appmango.net/anthonyjones/wp-content/uploads/2015/09/results-screens.jpg 1200w" sizes="(max-width: 1200px) 100vw, 1200px"></div></p>
<div class="image-caption center-align hide-on-large-only">Mobile results screen for responsive design</div>
<h4 class="light grey-text text-darken-1">Bookmarks</h4>
<aside class="aside-left hide-on-med-and-down"><i>I felt like it would be a good idea to keep bookmarks in the same content area as the results, so users wouldnt have to navigate to a different page and then back. Lets see what the users say during testing!</i></aside>
<p><div class="material-placeholder"><img src="http://appmango.net/anthonyjones/wp-content/uploads/2015/09/bookmarks.jpg" alt="Bookmarks Page Screen" width="1200" height="1000" class="materialboxed radius-three responsive-img aligncenter size-full wp-image-1481 intialized" srcset="http://appmango.net/anthonyjones/wp-content/uploads/2015/09/bookmarks-300x250.jpg 300w, http://appmango.net/anthonyjones/wp-content/uploads/2015/09/bookmarks.jpg 1200w" sizes="(max-width: 1200px) 100vw, 1200px"></div></p>
<div class="image-caption center-align hide-on-large-only">I felt like it would be a good idea to keep bookmarks in the same content area as the results, so users wouldnt have to navigate to a different page and then back. Lets see what the users say during testing!</div>
<h4 class="light grey-text text-darken-1">History Page</h4>
<aside class="aside-left hide-on-med-and-down"><i>This screen keeps all temporary history and search data. Users can delete history or permenantly save to their accounts</i></aside>
<p><div class="material-placeholder"><img src="http://appmango.net/anthonyjones/wp-content/uploads/2015/09/history.jpg" alt="History Page" width="1200" height="1000" class="materialboxed radius-three responsive-img aligncenter size-full wp-image-1477 intialized" srcset="http://appmango.net/anthonyjones/wp-content/uploads/2015/09/history-300x250.jpg 300w, http://appmango.net/anthonyjones/wp-content/uploads/2015/09/history.jpg 1200w" sizes="(max-width: 1200px) 100vw, 1200px"></div></p>
<div class="image-caption center-align hide-on-large-only">This screen keeps all temporary history and search data. Users can delete history or permenantly save to their accounts</div>
<h4 class="light grey-text text-darken-1">Saved Searches</h4>
<aside class="aside-left hide-on-med-and-down"><i>Permanently stored saved history data</i></aside>
<p><div class="material-placeholder"><img src="http://appmango.net/anthonyjones/wp-content/uploads/2015/09/saved-searches.jpg" alt="saved-searches" width="1200" height="1000" class="materialboxed radius-three responsive-img aligncenter size-full wp-image-1480 intialized" srcset="http://appmango.net/anthonyjones/wp-content/uploads/2015/09/saved-searches-300x250.jpg 300w, http://appmango.net/anthonyjones/wp-content/uploads/2015/09/saved-searches.jpg 1200w" sizes="(max-width: 1200px) 100vw, 1200px"></div></p>
<div class="image-caption center-align hide-on-large-only">Permanently stored saved history data</div>
</div>
