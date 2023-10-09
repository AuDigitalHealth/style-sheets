## Change Log/Revision History

---
### > Generic Style Sheet Revision Log
---
The below is a history log of changes made to the style sheet.
There are 2 versions of the style sheet, with a different look and 
feel. v1.1 has java script which caused some issues with rendering
and was taken out in v1.2. Also the main changes included moving
the "more administrative details" to the bottom of the document so
the clinician could see straight about the "clinically relevant" 
data first without having to scroll down the page. Section headers
and indentations were also introduced for better readability.

Version 1.1.x, 1.2.x will not me maintained any further unless any major 
bug is found.
Version 1.3.x will continue to be maintained adding any further
functionality deemed necessary or requested.

#### DH_Generic_CDA_Stylesheet-1.7.4 | 09/10/2023
---
- Fix Version number
- Added support for Gender Identity originalText

#### DH_Generic_CDA_Stylesheet-1.7.3 | 05/10/2023
---
- Fix Bug NAME to name
- Added support for Gender Identity


#### DH_Generic_CDA_Stylesheet-1.7.2 | 26/05/2023
---
- Tidy up css
- Support for https in electronic medium
- Added test for all other Communication Medium types
- Added variable to make contact websites clickable - off by default
- Added NOT - Urgent Notification Contact for Participant
- Added support for HL7 fhir gender types
- Added support for ACTS documents
- Added support for MyMedicare Registered Practice Information

#### DH_Generic_CDA_Stylesheet-1.7.1 | 11/02/2022
---
- Fix issue around Encounter details not showing in Admin Details section for other docs
- Param added to hide Admin Details

#### DH_Generic_CDA_Stylesheet-1.7.0 | 01/09/2021
---
- Added Title for iFrame document types for screen readers
- Fixed up css styles inc Contrast colour 4.5:1 for gray shades
- Added downloadedFromMyHRDT param to allow systems to add the date downloaded to appear 
  in the the Administrative Details section (for viewing and printing)
- Include support for originalText for Title of CDA document

#### DH_Generic_CDA_Stylesheet-1.6.0 | 23/07/2019
---
- Added ACSQHC recommendations as per document:
  National-guidelines-for-on-screen-presentation-of-discharge-summaries-Feb-2018.pdf
  Updated 3 headers text, Font Sizes, Uppercase all SURNAMES, added LoS
- Added space after Author name and before specialty
- Removed redundant attributes (eg summary, valign)
- Addressed Usability issues
- Improved age display
- Added captions to tables with hidden text for screen readers
- Moved Styles out into CSS
- Param for widescreen mode
- Added additional Javascript detection when whitespace chars used
	
#### DH_Generic_CDA_Stylesheet-1.5.0 | 20/12/2018
---
- Added OID for PCML
- Removed escaped space before Participant Header
- Added support for iFrame to display PDFs in certain doc types (default off)
- Updated PCML to PSML description
- Added hidePatientContactDetails param to allow override masking patient address 
  and other contact details for documents obtained from My Health Record, the default is true
	  
#### DH_Generic_CDA_Stylesheet-1.4.0 | 11/07/2017
---
- Added optional HPI-O for certain Recipient scenarios (asOrganizationPartOf)
- Added optional HPI-O for Author, Responsible HP for DS and Requester
- Fixed up every location where &lt;xsl:call-template name="addID"&gt; is called before 
  &lt;attribute&gt; rather than after. Affected cda:list, cda:table and cda:paragraph
- Added support for Service Referral

#### DH_Generic_CDA_Stylesheet-1.3.0 - 06/01/2017
---
- Updated Owner The Australian Digital Health Agency
- Removed display of data element hierarchy
- Replaced NEHTA with DH for env variables
- Replaced PCEHR with MHR for env variables
- Added OID for AIR 
- Added display of captions within paragraph elements
- Added display of captions within list items
- Added display of author's organisational address and communication details 
- Added support for originalText for Author Role
- Added support for originalText for Separation Mode
- Added check for correct OID for IHI
- Added additionalLocator to display of addresses 
- Added direction to display of addresses
- Added display of nullFlavor for addresses
- Added display of nullFlavor for electronic communication details
- Added display of nullFlavor for Separation Mode
- Added display of nullFlavor for patient's familyName
- Added display of nullFlavor for encounter timestamps (for Discharge Summary and Event Summary)
- Tracked changes rendered as final version
- Added stylesheet parameter "showProviderHomeDetails" to indicate if personal contact details and addresses (those marked as
  home) are to be rendered. 
- Fixed "Responsible Health Professional At Time Of Discharge" to display contact details if present.
- Fixed event summary to display encounter period accordingly if only end date is specified.
- Fixed display of provider contact details to say "Not provided" when unavailable.

#### NEHTA_Generic_CDA_Stylesheet-1.2.9 - 04/11/2014
---
- Fixed WCAG color contract issue with Title headers and administrative details
- Added Pathology, DI and ACI object identifiers (OIDs)for document type lookup
- Fixed CSS syntax issues related to width
- Updates processing for table body, table head, and table row elements
- Added bannerDisplay parameter. When set to a value of 'false', will disable 
  generation of the fixed Banner for Rendering Systems which already display
  the banner elsewhere. Default is to always display the Banner.
- Changed Document Type name of the Medicare View from "Medication Information View"
  to "Medicare Overview"
- Updated document type names:
    - "e-Discharge Summary" changes to "Discharge Summary"
    - "Australian Childhood Immunisation Register Record" to "Australian Childhood Immunisation Register"
    - "Consumer Entered Notes" to "Personal Health Note"
    - "Consumer Entered Health Summary" to "Personal Health Summary"
    - "PCEHR Prescription Record" to "eHealth Prescription Record"
    - "PCEHR Dispense Record" to "eHealth Dispense Record"
- Provided constants for clinical document type names to simplify implementation of any future name changes
- Fixed bug to display Referee participant contact details for e-Referral
- Added Rendering of Occupation and Qualifications for:
  a) general Participants
  b) general Recipients
  c) e-Referral Referee
  d) Specialist Letter Referrer
- Improved checking of background and foreground text colour style code values
- Improved checking of em and pixel font size style code values
- Improved checking of table cell column width style code values
- Fixed a bug in which column width style codes were not being processed correctly
- Added checking for JavaScript references in linkHtml links,  and renderMultimedia targets, and the Logo target
- Added rendering of Requester participants and Order ID in Pathology Report and Diagnostic Image Report 
- Added rendering of Accession ID for Diagnostic Image Report

#### NEHTA_Generic_CDA_Stylesheet-1.2.8 - 22/10/2013
---
- Fixed bug in nestedSection template
- Fixed author name bug at start of document
- Added parameter to disable rendering of the Administrative Observations section (defaults to always displaying it)
- Fixed td and th templates to correctly assign generic CSS styles when an 'ID' attribute is present
- Added Banner CSS styles to support Microsoft Internet Exporer 6
- Added status of withdrawn documents to the banner
- Added Street Suffix, Postal Delivery Type, Postal Delivery Number, Australian Unit Number and Australian Unit Type
  to display of addresses
- Administrative Observations section will only be rendered if the narrative block &lt;text&gt; element is present in the section
- Removed page-break-inside: avoid CSS property throughout

#### NEHTA_Generic_CDA_Stylesheet-1.2.7 - 22/12/2012
---
- Fixed footnoteRef bug
- Removed commented out code in cda:footnote template

#### NEHTA_Generic_CDA_Stylesheet-1.2.6 - 10/12/2012
---
- Updated linkHtml to support observationMedia internal targets and external targets
  (i.e. those without an XML ID e.g. a file in the package or external URL)
- Added PCEHR Prescription and Dispense View document type recognition
- Ensured consistent date/datetime date/month/year separators when formatting dates
- Changed formatting of patient name in the banner

#### NEHTA_Generic_CDA_Stylesheet-1.2.5 - 03/10/2012
---
- Included Author Organisation and Author Department in administrative details  

#### NEHTA_Generic_CDA_Stylesheet-1.2.4 - 27/09/2012
---
- Amended display of document, set, and related identifiers      
- Removed display of PCEHR Prescription Record and PCEHR Dispense Record
  item identifiers in Administrative Details

#### NEHTA_Generic_CDA_Stylesheet-1.2.3 - 14/09/2012
---
- Added printing of the Black Banner on the first page
- Trimmed the content of the HTML title for printing
- Fixed top left margin alignment for xPre text
- Added param to support displaying style sheet version

#### NEHTA_Generic_CDA_Stylesheet-1.2.2 - 03/09/2012
---
- Added "PCEHR Prescription + Dispense" record document type
- Fixed paragraph wdith issue within a table.

#### NEHTA_Generic_CDA_Stylesheet-1.2.1 - 31/08/2012
---
- Corrected "Medicare/DVA Benefits Report" document type name
- Fixed section header attribute bug

#### NEHTA_Generic_CDA_Stylesheet-1.2.0 - 20/08/2012
---
- New Version - reformatted look and feel to align with PCEHR view
- Removed java script
- Parameterised the display of HPI-I, HPI-O and PIO-D with def.false
- Changed wording for Incompatibility message (also does not popup)
- Added OIDS for Consolidated and Medicare views
- Adjusted width to allow a min and max to allow for sizing
- Age Calculation uses Admin Obs if present otherwise gives age in
  days weeks, months or years
- Added Indigenous Status
- Added Discharge Location
- Added Support for full range of encompassingEncounter effectiveTime
  values (low, high, value, unit)
- Move All Admin Details to bottom as well as Admin Observations
- Fix Logo bug for non-PNG image types

#### NEHTA_Generic_CDA_Stylesheet-1.1.12 - 03/09/2012
---
- Fix Logo bug for non-PNG image types
- "July" should be "Jul"
- Add OIDs for PCEHR Prescription Record and PCEHR Dispense Record 
  and other new CDA document types
- Add Transform Status Indicator
- Location of Discharge
- Add Entitlements for orgs and subject of care
- Support for Author Devices
- Date of birth calculation algorithm
- Order of sections (Admin Obs at end)

#### NEHTA_Generic_CDA_Stylesheet-1.1.11 - 06/07/2012
---
- Added http-equiv X-UA-Compatible meta tag to support browser 
  compatibility mode so when printing, sections aren't broken up
- Fixed formatting of address supporting different address line
  combinations adding commas where necessary

#### NEHTA_Generic_CDA_Stylesheet-1.1.10 - 06/07/2012
---
- Applied WCAG v2 AAA standards - accessibility
- Fixed up &lt;dl&gt; tag issue around contact details

#### NEHTA_Generic_CDA_Stylesheet-1.1.9 - 19/06/2012
---
- Added referees to list of participants displayed
- Added support for D/S using encompassingEncounter effectiveTime for 
  encounter details section
- Added author address to author section

#### NEHTA_Generic_CDA_Stylesheet-1.1.8 - 19/06/2012
---
- Applied WCAG v2 AAA standards - accessibility
- Fixed up &lt;dl&gt; tag issue
- Added new production license agreement

#### NEHTA_Generic_CDA_Stylesheet-1.1.7 - 14/06/2012
---
- Applied WCAG v2 AAA standards - accessibility
- Moved headers out of tables
- Converted tables to definition lists &lt;td&gt;.. to  &lt;dl&gt;&lt;dt&gt;&lt;dd&gt; for WCAG
- Standardised organisation details into a &lt;template&gt;
- Added support for gif and jpeg for LOGO (was just png)

#### NEHTA_Generic_CDA_Stylesheet-1.1.6 - 07/06/2012
---
- Only show DOB date (not time)
- Age Calc uses encompassingEncounter effective time if present
- Moved facility name from around Logo
- Reformatted participant tables from &lt;td&gt; to &lt;th&gt; changing the &lt;style&gt; 
  code as well
- Changed section header &lt;style&gt; from &lt;h2&gt; to a &lt;div&gt;
- Removed unused &lt;template&gt;s

#### NEHTA_Generic_CDA_Stylesheet-1.1.5 - 28/05/2012
---
- Added additional http-equiv values to support java script and text/css
- Added formatDate &lt;template&gt;

#### NEHTA_Generic_CDA_Stylesheet-1.1.4 - 22/05/2012
---
- Tidied up support for different mediaTypes and how to display them 
  (or provide links to them)
- Added support for rendering the Logo
- Added validation when splitting a hi identifier into 4-4-4-4

#### NEHTA_Generic_CDA_Stylesheet-1.1.3 - 21/05/2012
---
- Adjusted banner format
- Added OID for Advance Care Directive

#### NEHTA_Generic_CDA_Stylesheet-1.1.2 - 14/05/2012
---
- Adjusted banner display when ihi or mrn not present
- Fixed imag/tiff to image/tiff

#### NEHTA_Generic_CDA_Stylesheet-1.1.1 - 02/05/2012
---
- Display patient's first name
- Add IHI and MRN to banner
- Add additional support for application/rtf + application/xml
- Trimmed leading and trailing spaces on prefix suffix given and family 
  names when concatenating
- Removed seconds from date time display (and us time zones)

#### NEHTA_Generic_CDA_Stylesheet-1.1.0 - 20/03/2012
---
- First published version 

<br><br>

---
### > PCEHR_Prescription_and_Dispense_View Style Sheet Revision Log
---
The below is a history log of changes made to the style sheet.

#### NEHTA_PCEHR_Prescription_and_Dispense_View_CDA_Stylesheet-1.1.1 - 25/11/2020
---
	- Updated Owner The Australian Digital Health Agency
	- Updated description removing the PCEHR from title
	- Replaced NEHTA with DH for env variables
	- Replaced PCEHR with MHR for env variables
	- Update JQuery to v3.5.1

#### NEHTA_PCEHR_Prescription_and_Dispense_View_CDA_Stylesheet-1.1.0 - 28/03/2013
---
- Added "no grouping" functionality
- Added parameter to exclude Prescription Items when no grouping is used
- Added parameter to exclude Dispense Items when no grouping is used
- Updated Group By information in the Banner to include exclusions if active
- Added Dispense Number (e.g. 'Initial Dispense', 'Repeat 1', etc.) to dispense
  document lines when 'Number of this Dispense' value is present
- Added Number of Dispenses (e.g. 'Dispense original and 0 repeats') to
  prescription document lines
      
#### NEHTA_PCEHR_Prescription_and_Dispense_View_CDA_Stylesheet-1.0.1 - 20/03/2013
---
- Bug fix when grouping by brand name. Previously Dispense or Prescription
  Item rows were being left out of the grouping if they had an originalText
  Therapeutic Good Identification value which was the same as a previously 
  grouped item which had the same value as a displayName but with a different
  originalText value.
- Bug fix when grouping by brand name. Summary lines were not being sorted
  correctly.
- Bug fix when document type for PCEHR Prescription & Dispense View in the
  Administrative Details and HTML title.

#### NEHTA_PCEHR_Prescription_and_Dispense_View_CDA_Stylesheet-1.0.0 - 06/03/2013
---
- First published version 



---
### > DH_Diagnostic_Imaging_And_Pathology_View Style Sheet Revision Log
---
The below is a history log of changes made to the style sheet.

#### DH_Diagnostic_Imaging_And_Pathology_View_CDA_Stylesheet-1.1.2 - 10/12/2020
- Headers in path report for specimen and report date the wrong way around

    
#### DH_Diagnostic_Imaging_And_Pathology_View_CDA_Stylesheet-1.1.1 - 19/06/2018
---
- Updated initial version to align with Presentation Guide
- Updated to match presentation guide

