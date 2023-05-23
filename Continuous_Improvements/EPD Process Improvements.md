EPD Process Improvements

# EPD Feedback
February 27, 2023

[Hardware/Software Requirements Ownership in Jama: ](https://sdlc.electrolux.com/browse/UEAROD-124)
Change the name of this document from “[​E-SW Requirements Specification](https://electrolux.sharepoint.com/sites/innovationactivation2/Electronics/Deliverable%20Templates/GEO-xCA-ENG-T-00075_E-Software%20Requirements%20Specification%20Template.docx)” and “[​ E-HW Requirements Specification](https://electrolux.sharepoint.com/sites/innovationactivation2/Electronics/Deliverable%20Templates/GEO-xCA-ENG-T-00076_E-Hardware%20Requirements%20Specification%20Template.docx)” to “Behavior / Performance Requirements.”  The name of this document is completed by the Systems Engineers and should describe the Behavior and Performance requirements of the system, and is NOT a Software or Hardware Requirements Specification to remove confusion as to the content of the document and the owner, rather than the name implying an competency.

Jama shall be the one repository for Non Functional and Functional Requirements, removes redundancy from one EPD document to another for reuse of artifacts, version control, and duplication of information across different EPD Templates.
1. [Requirement Analysis Review documentation:](https://sdlc.electrolux.com/browse/UEAROD-117)  Referring to the Requirements Elicitation Process, when using the Jama tool for requirements management, can we use built-in capabilities of Jama for our review process rather than the separate E-Requirements Analysis Review document?
1. [Project Feasibility](https://sdlc.electrolux.com/browse/UEAROD-132) - E-Design Requirements Specification - Create
1. [GEO-xCA-ENG-T-00074_E-Electronic Functional Prototype Requirements](https://sdlc.electrolux.com/browse/UEAROD-134)
1. [GEO-xCA-ENG-T-00073_E-Design Requirements Specification Template and GEO-xCA-ENG-T-00026_E-Requirements Analysis Review](https://sdlc.electrolux.com/browse/UEAROD-150)
1. [GEO-xCA-ENG-T-00073_E-Design Requirements Specification Template](https://sdlc.electrolux.com/browse/UEAROD-151)
1. **Requirements Versioning:**  Using Jama for requirements management and version control of requirements will resolve a conflict the Sysems Engineers have recorded and “Stephen Garrison” has documented in the word template on 10/18/2018:
    1. “All documents referenced in this section must include the Revision and Revision date, with the exceptions being for Electrolux Standards having only the revision and Other Documents having revision and/or date where applicable.”
    1. Corrective Action to Resolve:  Jama will do the revision control for you and not require manual entry, as this was documented on 10/18/2018 and is still in EPD1.0 and EPD 2.0 we would suggest converting to Jama for Requirements Management and integrating these templates into Jama.
1. [Document ID’s Document IDs for Requirements Documents:](https://sdlc.electrolux.com/browse/UEAROD-110)  Requirements will be created in Jama, exportable as documents for Teamcenter.  What would be the purpose to create distinct Document IDs outside of Teamcenter system?  Would this only apply if requirements are not originally created within Jama? 
    1. Corrective Action to Resolve:  In Jama this is done automatically and revision controlled
1. Traceability of Requirements.  Requirements in the documentation is created to all levels (Stakeholder, Product Line, Electrical/Electronic Systems, Subsystems, Module and Component) however it is impossible to differentiate in the word document within the EPD 2.0 Process and recommendation would be to use the capabilities and workflow within Jama to document these levels of requirements.  The Jama tool will also identify when a higher level requirement is changed by notifying of a higher level change that impacts the lower level solutions.
1. Included in Jama Tool and Available of these areas that can drive efficiencies within the EPD Process:
    1. [Systems Architecture Documentation:](https://sdlc.electrolux.com/browse/UEAROD-126)  In reference to E-System Architecture documentation defined in the E-Architecture Design Process, can we consider using Jama to manage all this content instead?
    1. [System Bill of Materials:](https://sdlc.electrolux.com/browse/UEAROD-127)  Referring to System Bill of Materials as defined in E-Architecture Design Process, what is intended as the input to System Bill of Materials?  Where will these costs be managed?  Is this a database of components and costs managed by the hardware team?
    1. [E- Systems Test Design:](https://sdlc.electrolux.com/browse/UEAROD-128) The E-Verification and Validation Process defines E-System Test Design deliverable to include testing procedure for a system.  However, the plan should be to create the testing procedure for each requirement inside Jama, so that we can trace the link between requirements and test procedure and also to make the test procedures reusable as requirements are shared across projects.
    1. [E-System Test Execution Report:](https://sdlc.electrolux.com/browse/UEAROD-129)  As an extension of previous comments on E-System Test Design, the E-Verification and Validation Process defines for the Lab to document testing results and execution detail into this System Test Execution Report.  However, could this be done entirely in Jama instead and then exportable to our processes (EPD, Teamcenter, etc)?
1. [GEO-xCA-ENG-D-00010_E-Architecture Design Process - Task 9:](https://sdlc.electrolux.com/browse/UEAROD-130)  How does this differ from a component BOM and how can we  estimate if Solutions Architects select the EDMs to meet the System requirements?
1. [GEO-xCA-ENG-D-00013_E-V&V Process - Task 21, 36, 57, 75:](https://sdlc.electrolux.com/browse/UEAROD-131)
    1. Review and approve test results (Design Verification) - Should SY-IN and/or SY-AR be listed as Support or Inform?
    1. Review and approve test results (SW Validation) - Should SY-IN and/or SY-AR be listed as Support or Inform?
    1. Review and approve test results (Design Verification - HW Unit (Bench) Testing) - Should SY-IN and/or SY-AR be listed as Support or Inform?
    1. Review and approve test results (Tool Verification - Unit (Bench) Testing) - Should SY-IN and/or SY-AR be listed as Support or Inform?
Jira shall be the one repository for Project Status, removes redundancy from one EPD document to another for Project Issues, Tracking Timelines to duplication of information across different EPD Templates.
Link EPD Process on Sharepoint to the Physical Document.
As an example EPD Process Deliverables([E-Hardware Requirements Specification - Final](https://electrolux.sharepoint.com/sites/innovationactivation2/Pages/Electronics/Product-Concept-Def-&-Validation.aspx)) to the Physical Templates ([E-HW Requirements Specification](https://electrolux.sharepoint.com/sites/innovationactivation2/Electronics/Deliverable%20Templates/GEO-xCA-ENG-T-00076_E-Hardware%20Requirements%20Specification%20Template.docx)) somehow to have direct access to the document being requested per the EPD Process.
[Configuration and Development Tools Roles](https://sdlc.electrolux.com/browse/UEAROD-125): Besides for the DT-CL (Antonino), do we know who is assigned for these other roles?

 
Each Individuals Feedback from Jira about the EPD 2.0 Process for your further review.
Saili Ghavat- [Task to review EPD 2.0 in Jira](https://sdlc.electrolux.com/browse/UEAROD-112)
Justin Woehler - [Task to review EPD 2.0 in Jira](https://sdlc.electrolux.com/browse/UEAROD-114)
Sandro Tarquini - [Task to review EPD 2.0 in Jira ](https://sdlc.electrolux.com/browse/UEAROD-113)
Richard A Martin - [Task to review EPD 2.0 in Jira](https://sdlc.electrolux.com/browse/UEAROD-115)
