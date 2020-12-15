# Introduction

This page has been created to give you the opportunity to download and engage with the correlations we've created thus far. We value your feedback so please answer the questions below and share any thoughts or suggestions you may have.
The purpose of the correlation relationships published is to demonstrate the importance of recognising correlation relationship data model for practical applications, and thus propose it to data producers, software vendors, and researchers to consider it for adoption.

Note that the Correlation Relationships produced are experimental data and fall under the Experimental Statistics category. The methodologies used to develop the correlations are under development and would require further extensive testing. 

This means that the data:
- may not be complete or fully developed;
- may contain inaccuracies; and
- could be subject to changes based on user feedback.

Note that there is no guarantee as yet on whether participating partner bodies will continue to be able to generate the correlations.

The Office for National Statistics (ONS) has a useful 
[Guide to Experimental Statistics](https://www.ons.gov.uk/methodology/methodologytopicsandstatisticalconcepts/guidetoexperimentalstatistics).


## How you can help

We would be very grateful for any input or comments that you may have but specifically would welcome your thoughts on the following questions:

1.	Is anything missing from this data model?
2.	Is there anything that would need to be changed in order for your organisation to consider adopting?
3.	Which aspects do you consider the most valuable to your organisation and users?
4.	Do you have any suggestions for how we can maximise future engagement with this work?
5.	What other correlation relationships could be of interest to you?
6.	What other correlation relationship data models do you know of that we could possibly research?

<a href="http://www.google.com/">
    <button>Feedback form</button>
</a>



![Correlation between different entities](/_media/Correlations.png, width="400")


We developed a correlation relationship data model which was tested against three correlation relationships. These are listed below:
- OS MasterMap Topographic Area Polygon and HM Land Registry Inspire Polygon
- Different forest representations used by Defra and OS
- VOA Property Address and OS AddressBase Property Address
## What are our goals?
- To verify that the Correlation Relationship data model effectively represents the correlation between the datasets;
- Does the Correlation Relationship data model support the FAIR (link) principles:
    - Findability – is it easy to find
    - Accessibility – was it easy to access
    - Interoperability – does the data model metadata support integration. 
    - Reusable –  ….
- Identify areas of improvement (talk about improving data governance, ethical issues in sharing, TQV).
## Related Literature
- The motivation underlying the interest in correlation relationship is similar to those of probabilistic data linkage techniques used for Master Data Management. 
- Probabilistic record linkage is widely used across the government. For example, Ministry of Justice [2], ONS [3] and Home Office [4], where the similarity between related datasets, typically records on individuals, is derived to create a Master Data using sophisticated algorithms in open source. (e.g. See [2]) and commercial off the shelf software such as IBM Big Match and Informatica R (Dan Rickman, Home Office Data Scientist, personal communication).
- The main emphasis of the probabilistic record linkage is to find the similarities and deduplicate records. However, at the time of writing this project didn’t find any evidence of any dedicated focus on the capture of the metadata behind probabilistic record links, in the elaborate and transparent manner as proposed by this project. However, it is reasonable to speculate that it would of course be possible to do so easily when needed. 

### References
[1] [VOA rating list downloads](https://voaratinglists.blob.core.windows.net/html/rlidata.htm) (accessed 22/11/2020)
<br>[2] [ISO 19160-4:2017](https://www.iso.org/standard/64242.html) (accessed 22/11/2020)
<br>[3] [BS7666 Guidelines](https://www.agi.org.uk/agi-groups/standards-committee/bs7666-guidelines) (accessed 22/11/2020)
<br>[4] [AddressBase Premium](https://www.ordnancesurvey.co.uk/business-government/products/addressbase-premium) (accessed 22/11/2020)
