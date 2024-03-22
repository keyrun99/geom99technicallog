# geom99technicallog
Publish Rest Service link to ArcGIS Online 
Start time : 16 March (8: 00 PM)
Finished time : 16 March (8.15 PM)
Time spent about : 15 minutes
Tutorial Link (if any):

1.	Get the link from the open source (done by Group member) compiled in https://github.com/cklouislok/geom99web7/blob/main/data.md 
2.	Login to the ArcGIS online and to Content and to New Item and to URL option
3.	In the new pop-up window of the new item add the Rest Server link and click Next and add the designated Title, Tags and Summary and then Save. (This will create a feature layer with the Title you mentioned)
4.	The feature layer will be created in ArcGIS online. Open the map in map Viewer and check on the details and attributes
5.	Save the map two different layer. One in Web Map and the other in Web Scene (Web Map is a 2d map, while Web Scene is a 3d map)
6.	Share the web map and Web scene with Everyone (Public)
Public the ArcGIS Online map through Experience Builder
Start time : 15 March (8:20 PM)
Finished time : 15 March (9.40 PM)
Time spent about : 80 minutes
Tutorial Link (if any): https://www.youtube.com/watch?v=6e7Q6sN-kcs 
https://www.esri.com/en-us/arcgis/products/arcgis-experience-builder/overview 
ArcGIS Experience Builder is the modern tool to configure web apps without writing code. Build mapcentric or nonmapcentric apps and display them on a fixed or scrolling screen, on single or multiple pages using this tool (it largely replaces webapp builder). Perform a drag-and-drop operation to choose the tools you need from a rich set of widgets, design your own templates, and interact with your 2D and 3D content—all within one app. With ArcGIS Experience Builder, your web apps look great and run seamlessly on mobile devices.

1.	Go to Experience Builder through https://experience.arcgis.com/
2.	Go to Create New and choose the template you would link. I choose Launch Pad Template for this trial and click create
3.	Name the Title as “Robbery Toronto App” or as per requirement
 

4.	Add data source (both Web Scene and Web Map) which is already published in the AGOL.
 
5.	Add New Page and Map and link the map to 
 
6.	Save and draft and preview the details. (The icons are at the top of the page)
 
7.	Change the layout options as required and Publish the map.
8.	Go back to ArcGIS online and share the map to Everyone(Public)
9.	There’s the URL link at the bottom of the item page on the ArcGIS online.

Using DuckDNS to create free DNS entry pointing to temporary IP address
Start time : 18 March (9 PM)
Published time : 18 March (9.23 PM)
Time spent about : 23 minutes
Tutorial Link: https://www.youtube.com/watch?v=8peq7B8SEYk

1.	Log into DuckDNS website or either create a new account to DuckDNS web platform https://www.duckdns.org/domains
 
2.	Create a new domain that has not been already created
3.	For this Geom99 VM server I am taking duwadi as domain
4.	Add ip address generated from VM so that the ip registered and the domain “duwadi.duckdns.org” works every time, when the ip address generated is updated here in Duck DNS.

Creating and Obtaining SSL Certificate
Start time : 18 March (9:25 PM)
Finished time : 18 March (10.11 PM)
Time spent about : 50 minutes
Tutorial Link: https://www.youtube.com/watch?v=eTNtJNn5j74

1.	Login to the Virtual Machine with the domain name created using duckdns
2.	Go to the browser and to the Win-acme and download the latest version of the software
 
3.	Extract the downloaded file and 
4.	Search iis in the search bar and open iis (internet information service (iis) manager)
 
5.	Go to GEOM99AGS2024 and to Sites and to Default web sites
 
6.	Go to Binding under Edit Sites at the right side of the screen. The pop up will appear with the settings. Select https and add the duckdns url duwadi@duckdns.org at the host name and put the SSL certificate to the defaults and select OK and CLOSE to all the popups and to the iis
 
7.	Check the error with the dns url in the edge
 
This is what we are going to fix using the ssl certificate
8.	Run the application wacs.exe as Run as administrator and update the form as instructed:

A simple Windows ACMEv2 client (WACS)
 Software version 2.2.8.1635 (release, trimmed, standalone, 64-bit)
 Connecting to https://acme-v02.api.letsencrypt.org/...
 Connection OK!
 Scheduled task not configured yet
 Please report issues at https://github.com/win-acme/win-acme

 N: Create certificate (default settings)
 M: Create certificate (full options)
 R: Run renewals (0 currently due)
 A: Manage renewals (0 total)
 O: More options...
 Q: Quit

 Please choose from the menu: n

 Running in mode: Interactive, Simple

 Please select which website(s) should be scanned for host names. You may
 input one or more site identifiers (comma-separated) to filter by those
 sites, or alternatively leave the input empty to scan *all* websites.

 1: Default Web Site (1 binding)

 Site identifier(s) or <Enter> to choose all: 1

 1: duwadi.duckdns.org (Site 1)

 Listed above are the bindings found on the selected site(s). By default all
 of them will be included, but you may either pick specific ones by typing the
 host names or identifiers (comma-separated) or filter them using one of the
 options from the menu.

 P: Pick bindings based on a search pattern
 A: Pick *all* bindings

 Binding identifiers(s) or menu option: a

 1: duwadi.duckdns.org (Site 1)

 Continue with this selection? (y*/n) - <Enter>

 Source generated using plugin IIS: duwadi.duckdns.org

Terms of service:    C:\ProgramData\win-acme\acme-v02.api.letsencrypt.org\LE-SA-v1.3-September-21-2022.pdf

 Open in default application? (y/n*) - <Enter>

 Do you agree with the terms? (y*/n) - <Enter>

 Enter email(s) for notifications about problems and abuse (comma-separated): duwadikiran31@gmail.com

 Plugin IIS generated source duwadi.duckdns.org with 1 identifiers
 Plugin Single created 1 order
 [duwadi.duckdns.org] Authorizing...
 [duwadi.duckdns.org] Authorizing using http-01 validation (SelfHosting)
 [duwadi.duckdns.org] Authorization result: valid
 Downloading certificate [IIS] Default Web Site, (any host)
 Store with CertificateStore...
 Installing certificate in the certificate store
 Adding certificate [IIS] Default Web Site, (any host) @ 2024/3/19 to store WebHosting
 Installing with IIS...
 Updating existing https binding duwadi.duckdns.org:443 (flags: 0)
 Committing 1 https binding changes to IIS while updating site 1
 Adding Task Scheduler entry with the following settings
 - Name win-acme renew (acme-v02.api.letsencrypt.org)
 - Path C:\Users\student\Downloads\win-acme.v2.2.8.1635.x64.trimmed
 - Command wacs.exe --renew --baseuri "https://acme-v02.api.letsencrypt.org/"
 - Start at 09:00:00
 - Random delay 04:00:00
 - Time limit 02:00:00
 Adding renewal for [IIS] Default Web Site, (any host)
 Next renewal due after 2024/5/13
 Certificate [IIS] Default Web Site, (any host) created

 N: Create certificate (default settings)
 M: Create certificate (full options)
 R: Run renewals (0 currently due)
 A: Manage renewals (1 total)
 O: More options...
 Q: Quit
Please choose from the menu:

9.	If you ever need to stop the VM and reopen it, we need to update the ip so the dns url can be running smoothly.
The DNS certificate looks like the one attached below:
 
10.	After obtaining SSL certificate the website Duwadi.duckdns.org looks likes this. The not secure issue during opening the link is fixed and is secure, which only needs to be refreshed after few months which is detailed in the SSL certificate.
  
 
Public the ArcGIS Online map through Dashboard
Start time : 19 March (8:40 AM)
Finished time : 19 March (9.55 AM)
Time spent about : 75 minutes
Tutorial Link (if any): https://www.esri.com/en-us/arcgis/products/arcgis-dashboards/resources 
https://www.youtube.com/watch?v=zrxYWzSvJ6E (2018 UC Presentation)
ArcGIS Dashboards present location data using interactive data visualizations on a single screen. Typically Dashboards are meant for managing or communicating information rolled-up into graphs and simple maps. The famous COVID-19 dashboard really "put this on the map". Tailor dashboards to your audiences, giving them the ability to slice the data to get the answers they need. Dashboards are essential information products, like maps and apps, providing a critical component to your geospatial infrastructure.

1.	Create a new dashboard with the title Toronto Neighborhood Map
 
2.	Go to add map at the left side of the screen ad select the map you have created on the AGOL. Go through the basic settings and Done to create the map.
 
3.	Select theme and set the theme as white or black, and check the other options as well
 
4.	Add Header and put the header at the top and add title and subtitle as wished. Go through the settings and have trials. We can add image as the title background and the logo as well.
 
5.	Select + icon and Add list, Customize and format the list (As we only got Event Id in the attributes table because of the sensible date, we are going to display the event ID only for this case, but for other data, there can be various options, check the 2nd attached screenshot as well)
 
 
6.	Add + and add indicator, select the layer, add descriptive text and Icon to describe the content
 
7.	To Modify Map Actions, Open map setting and ‘Map Actions’ to ‘When Map Extent Changes’ and Enable Indicator and  List then Zoom in to Review Results. (This will change the count and list when the map zoom extent is changed)
 
8.	Review results, Add charts and other aspects as required. To modify the map action go to the map extent setting and follow step7.
9.	Save the dashboard, the saved dashboard can be seen on the content of the AGOL. Share the map with the authorized user (to owner, organization or to everyone). The link which needs to be shared will be found at the bottom right side of the screen when we scroll the page.
The URL link for the recently created Dashboard is: https://www.arcgis.com/apps/dashboards/9e82f719a4d84c4aa6405ce9e0cc5832 which is shared for organization only as of now.

ArcGIS Solutions
Start time : 20 March (9:37 AM)
Finished time : 20 March (10:05 AM)
Time spent about : 40 minutes
ArcGIS Solution link: https://www.arcgis.com/apps/solutions/index.html?gallery=true&sortField=relevance&sortOrder=desc#home
# Didn’t get the concrete evidence in the solution but at least I tried
Esri's approach to developing configurable web solutions and software, which minimizes the need for custom development, offers several advantages and disadvantages. The Solutions site (linked here) provides a way to deploy ready-made complete solutions using the various configurable solutions. 

Here's a summary of advantages and disadvantages of Esri's configurable solutions:

Advantages:
Reduced Development Time and Costs: By offering configurable solutions, Esri allows organizations to implement sophisticated GIS applications without extensive custom coding, significantly reducing the time and financial investment required for deployment .

User-Friendly: Configurable solutions often come with intuitive interfaces and drag-and-drop functionalities, making it easier for non-technical users to customize and manage GIS applications according to their needs .

Flexibility and Scalability: Configurable solutions can be quickly adapted to changing business requirements or scaled to accommodate growth, without the need for significant redevelopment efforts .

Standardization and Reliability: Since the core software is standardized and extensively tested by the developer, it tends to be more reliable and secure than bespoke solutions, which may have unique bugs and vulnerabilities .

Disadvantages:
Limited Customization: While configurable solutions offer flexibility, they may not meet all the specific requirements of an organization. Some complex needs might still require custom development, potentially leading to a hybrid approach that can complicate system architecture.

Challenging to Change: Once deployed, configurable solutions can be challenging to modify and maintain as needs grow or evolve. Further, with 3 or 4 updates to the software in ArcGIS Online, things that once worked can suddenly break. Often the only way to fix them is to rebuild what was previously working from scratch. 
Dependency on Esri: Relying on configurable software solutions can lead to vendor lock-in, where an organization becomes dependent on Esri for updates, support, and new features. This can limit control over the software lifecycle and future direction .

Performance Overheads: Configurable systems, particularly those that offer a wide range of functionalities, can sometimes be less efficient than bespoke solutions optimized for specific tasks, potentially leading to performance issues in large-scale deployments .

Training and Skill Requirements: Although designed to be user-friendly, there is still a learning curve associated with configuring and optimizing these solutions. Organizations may need to invest in training for their staff to fully leverage the software's capabilities .

Esri's approach aims to balance flexibility with ease of use, catering to a broad audience while acknowledging the potential need for some level of customization. This strategy allows organizations to leverage powerful GIS capabilities without the extensive resources typically required for custom software development.
 
1.	Search “My Neighborhood service” in the search bar and select “Deploy Now”
 
2.	Hover over the My Neighborhood Services and Open the applications.
 
3.	Go to My Neighborhood Services at the Solution Contents and to configure
 
4.	Go to Configure
 
5.	“Select a Map” I selected Toronto Robbery Map 
6.	Go to Theme and Layout and select the layout panel size to small
 
7.	Publish the service and check the attributes
 
