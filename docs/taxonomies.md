---
title: "Taxonomies"
---

A variety of nonprofit activity codes have been created to describe missions and program activities. We have included two of the most common taxonomies, and some references for others. 

Machine learning techniques are also promising because they allow you to build your own taxonomies. You can then hand-code a small sample of the data, which is used as a training dataset to calibrate your machine learning algorithms ([for example](https://towardsdatascience.com/train-image-recognition-ai-with-5-lines-of-code-8ed0bdd8d9ba)), which can then code a large corpus of mission statements. We encourage you to think about creating your own purpose codes and sharing your approach. 


## NTEE Codes [ [NCCS: History and Overview](https://nccs.urban.org/project/irs-activity-codes) ]  [ [Codes](https://github.com/Nonprofit-Open-Data-Collective/machine_learning_mission_codes/raw/master/docs/assets/NTEE_Two_Page_2005.pdf) ]

**Major Groups:**

* I. Arts, Culture, and Humanities - A
* II. Education - B
* III. Environment and Animals - C, D
* IV. Health - E, F, G, H
* V. Human Services - I, J, K, L, M, N, O, P
* VI. International, Foreign Affairs - Q
* VII. Public, Societal Benefit - R, S, T, U, V, W
* VIII. Religion Related - X
* IX. Mutual/Membership Benefit - Y
* X. Unknown, Unclassified - Z

**Common Codes:** 

Common codes represent activities of organizations, such as research, fundraising, and technical assistance, which are common to all major groups. The seven common codes used are:

* 01 Alliance/Advocacy Organizations  
* 02 Management and Technical Assistance  
* 03 Professional Societies/Associations  
* 05 Research Institutes and/or Public Policy Analysis 
* 11 Monetary Support - Single Organization  
* 12 Monetary Support - Multiple Organizations  
* 19 Nonmonetary Support Not Elsewhere Classified (N.E.C.)  

## IRS Tax-Exempt Purpose Codes  [ See [Instructions pp 6-7](https://www.irs.gov/pub/irs-pdf/i1023ez.pdf) ]

When applying for tax exempt status from the IRS, nonprofit founders report organizational purpose codes on the 1023 form. These codes differ from the NTEE taxonomies in that each code is binary (yes/no), and they are NOT mutually exclusive, so a nonprofit mission can fulfill one or several of these purposes. Instructions for completing IRS 1023-EZ mission codes pp 6-7 [FORM](https://www.irs.gov/pub/irs-pdf/i1023ez.pdf).

The IRS has started releasing some of the meta-data for 1023-EZ forms, which allows us to incorporate the codes into the training dataset. 

* Charitable Purpose [yes/no]
* Religious Purpose [yes/no]
* Educational Purpose [yes/no]
* Scientific Purpose [yes/no]
* Literary Purpose [yes/no]
* Public Safety Purpose [yes/no]
* Amateur Sports Purpose [yes/no]
* Prevent Cruelty to Animals and/or Children [yes/no]



# Validity and Reliability of Codes

The challenge with many of the nonprofit activity codes is a noisy data that stems from two primary source:

* The ambiguous and evolving nature of nonprofit activities
* Poorly-constructed taxonomies

The main challenge with bad data is that trying to use supervised learning approaches to mission classification will inaccurate if the underlying taxonomy is meaningless or inconsistent. So good reliable input data is a prerequisite for accurate classifiers. 

We have approached this problem from a measurement perspective, and include discussion about the validity and reliability of each taxonomy. To measure the reliability of codes we have included a sample that was coded by three separate human beings to test for inter-coder reliability as a baseline metric when calibrating machine performance. We expect that codes which are difficult for humans to apply will also be difficult for machines to accurately predict. 

Human coded sample...

Rules for coding...

IRR scores...




# Additional Taxonomies

Some examples of alternative taxonomies that exist: 

* ICNPO Codes [ [Overview](http://asauk.org.uk/wp-content/uploads/2018/02/CNP_WP19_1996.pdf) ]  
* Candid (formerly Guidestar) [Philanthropy Classification System (PCS)](https://taxonomy.candid.org/resources/downloads) 
* Foundation Center Grant Taxonomy ([Subjects under the new PCS](https://taxonomy.candid.org/subjects/))  
* CLASSIEfier [ [LINK](https://www.ourcommunity.com.au/general/general_article.jsp?articleid=7593) ] 

The NTEE replaced the original IRS Activity Code taxonomy that was used until 1995. NCCS developed an [IRS Activity Code to NTEE Crosswalk](https://github.com/Nonprofit-Open-Data-Collective/irs-exempt-org-business-master-file#activity-codes) that was used to standardize codes for existing nonprofits.  



## References

Berlan, D. (2018). Understanding nonprofit missions as dynamic and interpretative conceptions.
Nonprofit Management & Leadership, 28(3), 413-422.

Barman, Emily. (2013). Classificatory Struggles in the Nonprofit Sector: The Formation of the National Taxonomy of Exempt Entities, 1969—1987. Social Science History. 37. 103-141. 10.2307/23361114.

Boris, E., & Mosher-Williams, R. (1998). Nonprofit advocacy organizations: Assessing the definitions, classifications, and data. Nonprofit and Voluntary Sector Quarterly, 27(4), 488-506. 

Boris, E. T., & Steuerle, C. E. (2006). Scope and dimensions of the nonprofit sector. The nonprofit sector: A research handbook, 66-88. 

Froelich, K. A., & Knoepfle, T. W. (1996). Internal revenue service 990 data: Fact or fiction?. Nonprofit and Voluntary Sector Quarterly, 25(1), 40-52. 

Grønbjerg, K. A. (1994). Using NTEE to classify non-profit organisations: an assessment of human service and regional applications. Voluntas: International Journal of Voluntary and Nonprofit Organizations, 5(3), 301-328.

Herman, R. D. (1990). Methodological Issues in Studying the Effectiveness of Nongovernmental and Nonprofit Organizations. Nonprofit and Voluntary Sector Quarterly, 19(3), 293–306. https://doi.org/10.1177/089976409001900309

Jones, Deondre’. IRS Activity Codes. Published January 22, 2019. https://nccs.urban.org/publication/irs-activity-codes

Salamon, L. M., & Dewees, S. (2002). In search of the nonprofit sector. The American Behavioral Scientist, 45(11), 1716. 

Salamon, Lester & K. Anheier, Helmut. (1992). In search of the non-profit sector II: The problem of classification. Voluntas. 3. 267-309. 10.1007/BF01397460.

Salamon, Lester M. and Helmut K. Anheier. "The International Classification of Nonprofit Organizations: ICNPO-Revision 1, 1996." Working Papers of the Johns Hopkins Comparative Nonprofit Sector Project, no. 19. Baltimore: The Johns Hopkins Institute for Policy Studies, 1996. [DOWNLOAD](http://asauk.org.uk/wp-content/uploads/2018/02/CNP_WP19_1996.pdf)

Smith, B. (1992). The Use of Standard Industrial Classification (SIC) Codes to Classify Activities of Nonprofit Tax-Exempt Organizations.

