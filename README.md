# Style Sheets

This is a software library that provides the Australian Digital Health Agency 
Generic CDA Stylesheet hereinafter referred to as the "Agency Stylesheet". 
The Agency Stylesheet is a reference implementation and may be used as a 
component of a CDA document Rendering System compliant to the Agency CDA 
Rendering Specification (CDA RS) in accordance to the requirements below. 
It remains your responsibility to test and validate the use of the 
"Agency Stylesheet" to make it production ready within a CDA document 
Rendering System.


Australian Digital Health Agency Stylesheet Overview
====================================================

The AgencyStylesheet is an XSLT 1.0 transform which transforms CDA
documents conforming to Agency CDA Implementation Guides and the CDA
Package Specification into an HTML 4.01 (CSS 2.1 and JavaScript 1.5)
document which may then be displayed in a web browser. 

The Agency Stylesheet together with a compliant Web Browser and an XSLT
Stylesheet processor software constitutes a Rendering System compliant
with the CDA RS.

In accordance with the CDA RS, the HTML document produced by the Agency
Stylesheet displays both the Banner and the Details of the header. The
Details of the header are separated into the following parts of the display:

 - A General Document panel containing the Document Metadata, Patient,
   Facility, and Encounter Details along with an Organisational Logo.
 - This panel is displayed near the top of the document under the fixed 
   banner and users may click a button to hide and reveal this section.
 - A Participants Panel which includes the details of the participants
   apart from the patient’s Nominated Primary Healthcare Providers
 - A Primary Recipients Panel which includes the details of the primary
   information recipients contained in the CDA document.
 - An Other Recipients panel which contains the details of any other
   (non-primary) recipient contained in the CDA document. This panel
   is displayed at the end of the document.
 - A Nominated Primary Healthcare Providers panel which contains the
   details of the patient’s Nominated Primary Healthcare Provider
   participants contained in the CDA document. This panel is displayed
   above the Other Recipients Panel.

The Agency Stylesheet transforms the narrative blocks in the Structured Body
of a CDA document into individual panels in the produced HTML document,
in the same order in which they appeared in the original CDA Document.

The Structured Body Section title elements in which each Narrative Block
is found will be included at the top of each of these panels and be clearly
highlighted. These panels will be displayed between the Primary Recipients
and Nominated Primary Healthcare Providers panels when the produced HTML
document is viewed.

Operational Requirements
========================

When using the Agency Stylesheet as part of a CDA RS compliant Rendering
System, the following operational requirements apply:

 - The Agency Stylesheet SHALL be executed using an XSLT 1.0 compatible
   processor.
 - The input CDA Document SHALL be conformant with existing Agency CDA
   Implementation Guides and the CDA Rendering Specification.
 - The output HTML document of the Agency Stylesheet SHALL be displayed using an
   HTML 4.01, JavaScript 1.5 and CSS 2.1 compatible rendering engine or software
   which employs such a rendering engine (e.g. a web browser).
 - Rendering Systems SHALL ensure the display they intend to view the HTML
   document produced by the Agency Stylesheet has a resolution of at least 
   1024x768 pixels. Note that this does not exclude smaller screen sizes (e.g.
   smart phones and tablets) if they allow scrolling the display to view the
   entire document. 
 - Rendering Systems SHALL provide appropriate input devices to allow a user to
   scroll through the entire document contents and view any PDF, RTF or text
   attachments.
 - The Agency Stylesheet execution does check the CDA Rendering Implementation
   Guide version if present in the CDA document. If a newer version of this
   guide is asserted in the CDA document, the Banner in the produced HTML
   document will alert the user and require input to display the rest of the
   document. 
 - The Agency Stylesheet presents the contents of the Banner as the document
   rendering view title as found in the title in the header of the produced
   HTML document.
 - Rendering Systems SHALL check the versions prior to executing the Agency
   Stylesheet.
 - Implementers are advised that current web browsers may allow users to define
   settings which might override HTML stylesheet elements. As this could
   potentially lead to clinically relevant information being rendered outside
   viewable screen space, it is suggested that appropriate measures are taken
   prevent this from occurring.
 - Rendering Systems using the Agency Stylesheet SHALL NOT allow users to
   override the presentation and style contained in the HTML produced by the
   Agency Stylesheet.
 - Rendering Systems using the Agency Stylesheet SHALL ensure that the title
   of the resulting HTML document produced is printed at the top of every
   page when printed.
 - Rendering Systems using the Agency Stylesheet SHALL ensure that the “Page
   N of T” marker is printed at the bottom of every page when the HTML
   document is printed.
 - Rendering Systems using the Agency Stylesheet SHALL ensure that background
   colours and images are printed when printing the output of the Agency
   Stylesheet.
 - Rendering Systems using the Agency Stylesheet SHALL ensure that the view is
   shrunk to fit the page when printing the output of the Agency Stylesheet.
 - The style sheet version can be displayed at the bottom of the document if
   the styleSheetVersionDisplay is set to true. If any modification is made to
   the style sheet, the version should be changed to reflect this and the 
   variable VERSION_NOTE should be changed to indicate that the style sheet
   is now a "vendor" version as opposed to the "Agency" one. This should never
   default to true in a production environment.
   
