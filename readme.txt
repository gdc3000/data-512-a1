Wikipedia Page Views using Wikimedia API
Author: Geoff Coyner

Overview
This project walked through the steps of pulling page view data since 2008 for desktop and mobile devices. This data is publicly available through the Wikimedia foundation APIs. An addition goal of this project is to use practice and show-case open scientific research best practices.

Getting Started
These instructions will get you up and running and explain the project, data and relevant files in more detail. The outputs of the data acquisition, processing and analysis steps are included and can also be reproduced using the included Jupyter notebook.

Before attempting to reproduce this work, please ensure that Jupyter notebooks is installed on local machine or accessible online and Python v3.6 is installed where appropriate.

Contents of this repo
This repo contains the following files:
	• 1 Jupyter notebook file outlining in detail the steps of data acquisition, processing and analysis. The other 
	• 5 .json files contained the raw data as provided by Wikimedia API, which are documented below..
	• 1 .csv file showing the intermediate output of the processing step outlined in the Jupyter notebook. The fields in this file are described in detail below.
	• 1 .png file which shows the  page views from Wikimedia for mobile and desktop since 2008. This file is the final output of the analysis outlined in the Jupyter notebook.
	• 1 Readme file
	• 1 License file

Relevant Documentation
This project is based on data from the Wikimedia pagecount and pageview API. The outputs of these APIs are described in more detail below.

The legacy Pagecounts API is documented here: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts. 

The Pageviews API is documented here: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews

Considerations
Fields in .csv file which are also used to generate the visualization (.png) are:
	• Year
	• Month
	• Pagecount_all_views
	• Pagecount_desktop_views
	• Pagecount_mobile_views
	• Pageview_all_views
	• Pageview_desktop_views
	• Pageview_mobile_views

The pagecount fields come from the Pagecounts API which has data dating back to January 2008. This data does not filter out spiders. The pageview fields are from the newer Pageviews API that does filter out spiders and contains data from July 2015 onward. This API also breaks out mobile into app vs. web traffic. These data are combined in the field pageview_mobile_views.

License
This project is licensed under the MIT License - see the license file for more details. 

The Wikimedia Foundation makes their data available under a Creative Commons Attribute-ShareAlike License.

Python is available under a modified GPL-compatible license. The packages matplotlib and pyplot are available under the same licenses.

The python package requests is available under an Apache license, version 2.0. The pandas package is available under the 3-clause BSD license.