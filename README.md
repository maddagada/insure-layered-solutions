# Insure-layered-solutions
The Impact of Known Vulnerabilities on Layered Solutions Team Project
## Executive Project Summary
The purpose of layered solutions is to give the ability of an institution to use layered commercial products to deliver access to their critical data while maintaining security.  Traditionally, government devices were designed and certified to be used to access their most sensitive data.  This is extremely costly and time consuming.  Recently, the government has been reviewing proposals which would utilize commercial devices to deliver the same results as the government devices.  To increase the governments assurance, the government is attempting to ascertain if the use of multiple or layered solutions will provide the level of assurance that a government device would deliver.

This task will attempt to determine the security benefit of using layered solutions in an institution and if it affords any advantages.  The two layers being investigated will be enterprise vpn solutions.  It will be prudent to research the National Vulnerability Database and the Common Vulnerabilities and Exposes database in order to create a timeline of vulnerabilities for enterprise solutions over the years at varying code levels.  It will be important to distinguish between the time the vulnerability is known and the time when the patch is released.  There is also another aspect to take into account.  It cannot be assumed that when the patch is released, that this will be the time that the institutions devices would be patched.  There will need to be a patch window, in which, an institution would review, test, and assign the patch to a change management request.  The research will need to be limited to only vulnerabilities that could possibility compromise a security layer.  The timeline will be developed to aid in displaying overlapping vulnerabilities of the layered solutions selected, if they exist.

It will be also important to ascertain the possibility of an adversaries' ability to compromise layered solutions that do not have overlapping timelines.  This would involve an adversary's ability to compromise one layer and then wait until the other solution has a new vulnerability known to it.  History has shown, in many cases adversaries will gain some access and sit and wait until another opportunity presents itself.  

Lastly, it will be important to research how long it takes an exploit to be created once the vulnerability is known.  This information will be easily identified as the timeline is created with vulnerabilities, patches and available exploits of vpn solutions. It will be important to also point out if there have been successful exploits of these vulnerabilities, not just hypothesized exploits that should be possible.

This is type of research is extremely important to all institutions to help protect sensitive data and mitigate the adversaries' ability to breach their network.  By compiling all of this data and creating a timeline to analyze this data, the hope is to provide useful information to confirms or denies the advantage of introducing layered solutions into an institutions network security posture.




## Proposed project timeline
![screenshot](https://github.com/MLHale/insure-layered-solutions/blob/master/GantCharts/GeneralGant.png)
## Risk list
| Risk Name (value) | Impact | Likelihood | Description |
|-------------------------------------------------------|--------|------------|:---------------------------------------------------------------------------------------------------------------------------------------:|
| Programming issues (64) | 8 | 8 | Any programming issues with the HTML webpage or the Python program will slow progress. |
|    Unable to find exploit and patch dates (63)        | 9 | 7 | If exploit and patch dates cannot be found or incorrect, the final results in the timeline will be off. |
| No vulnerability overlaps in timeline (56) | 8 | 7 | Problems could arise if the vulnerability timeline is not showing overlaps properly.    |
| Problems gathering data (18) | 6 | 3 | Any major issues scraping databases for information will not allow for the rest of the project to continue until data can be retrieved. |
| Team member availability (15) | 5 | 3 | Team members must be able to coordinate appropriate times to meet otherwise progress will be slowed. |
| CVEs not found (12) | 6 | 2 | The project will not work if relevant CVEs cannot be found for the Enterprise VPN solutions that have been chosen |

## Project Methodology
First vital step to this research project will be to define a set of enterprise vpn solutions.  Once the vpn solutions have been defined, a review of the National Vulnerability database and Common vulnerabilities and exposes database can be conducted.  In order to effectively extract data from the database the CIRCL CVE Search API will be utilized to collect as much data as possible about our VPN solutions and their vulnerabilities. A python script written by Matt Erasmus found on the CIRCL website appears to be the best option for collecting vulnerabilities separated by vendor. The data will need to be translated out of the JSON formatted output and another python script will be used in order to begin evaluating the vulnerabilities gathered and determine if they are relevant to this project. This evaluation will include searching for confirmed exploits, determining the impact on the layered solution, and collecting patch dates (if available). One definite possibility will be that one or more of our selected VPN providers may not have enough data available for inclusion in this project. This would result in removal from the vendor list.  Once the data set has been assembled and confident in the results, manual construction can begin by plotting the vulnerabilities on a timeline for each vendor and then compiling those timelines into a master. While compiling the timeline, programming will begin for our webpage which will be used it to display a vulnerability timeline based upon the selected vendors and search parameters.  Python and the Django web framework will be used for this site, barring any limitations found in the Django framework. The data will be held by a sql database.  The final step is to write documentation on the results and the webpage. Additionally, analysis of the overall exploitability of a layered VPN solution will be done and compared it to the vendor solutions. 
## Resources/Technology needed
Web server with appropriate software stack
## First Sprint Plan
![screenshot](https://github.com/MLHale/insure-layered-solutions/blob/master/GantCharts/ProposedProjectTimeline.png)
