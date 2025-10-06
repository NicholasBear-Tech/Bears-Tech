# Microsoft Purview Sensitivity Label Workbook Template

> [!CAUTION]
> This is still a work in Progress! It's in the final stages and ready to use, but we're still adding and changing things to better help people use and understand this tool to plan their Sensitivity Labels. 

Hello! The purpose of this Excel workbook Sensitivity Label template is to help you with planning out your Microsoft Purview Sensitivity Labels and to have something to show decision makers the architecture you're proposing to implement rather than walking them through the admin center and having to explain all of the parts in depth just to get to the part that you need them to make decisions on. This tool is meant to be used with the Secure by Default documentation in planning and mimics the admin center to help with easier deployment. I hope that this helps, and you have a wonderful day!

[Introduction to 'secure by default' with Microsoft Purview](https://learn.microsoft.com/en-us/purview/deploymentmodels/depmod-securebydefault-intro)

[Download the Workbook Here](https://github.com/NicholasBear-Tech/Bears-Tech/raw/refs/heads/main/Tools/Purview%20Sensitivity%20Labels%20Workbook/Sensitivity%20Label%20Workbook%20v0.9.9.xlsx)

## Explanation of Tabs

<img width="1024" height="22" alt="image" src="https://github.com/user-attachments/assets/131e7bad-76fb-4ec6-8db8-a0ee9bef7535" />

- How to use

    This tab is meant to help explain how to use the Workbook. 

- Sensitivity Labels

    This is meant to help with planning out your Sensitivity Labels. The following tabs go with this tab which is why they are the same color. Settings (Label Type & Scopes) here will directly affect your ability to use the name on the other tabs. 

    - Emails, Files, & Other Data
    - Teams meetings and chats
    - Groups & Sites

- Emails, Files, & Other Data

    This is meant to show the settings that you have for the Scope "Emails, Files, & Other Data" in the Sensitivity Label. This would be considered object based labeling scope.

- Teams meetings and chats

    This is to show the settings that you have for the Scope "Teams meetings and chats" in the Sensitivity Label. This would be considered object based labeling scope.

- Groups & Sites

    This is to the settings that you have for the Scope "Groups & Sites" in the Sensitivity Label. This would be considered container based labeling scope.

- Summary

    This is to see the overview of your Sensitivity Labels in a simpler manner to read for stakeholders or someone that needs to see all the labels and their configurations.

- Publishing

    This is to plan out your Sensitivity Label Publishing and its settings.

- Service-side Auto-Labeling

    This is to help you plan out your Auto-Labeling policies for Service-Side labeling.

- Data Loss Prevention (DLP)

    This template is meant to be for planning and deploying Sensitivity Labels, meaning that the DLP options are mostly text filled in and do not have all/most options like the other tabs since there are too many options to plan out in a nice manner for planning. It does have every section but not all options. This area is to plan out what DLP policies will be using Sensitivity Labels. I guess you could plan out the ones that don't have them as well since they're mostly filled in.

- Search

    This is to search any Label and or Policies to view what their settings are without jumping through the tabs to see.

## Explanation of the informational Section

<img width="107" height="172" alt="informational +" src="https://github.com/user-attachments/assets/63bdf58b-9d09-429b-a4d6-510017d8349f" /> <img width="107" height="110" alt="informational -" src="https://github.com/user-attachments/assets/e81ec4cd-e91c-44a8-9d33-9c7ff90348d1" />

In the workbook we have included a section on "Explanation" and "Links" to help explain that area and the appropriate links. The way to open and close it is the "+" or "-" sign on the left side of the workbook's numbers. 

## Usage

1. First you should read the "How to Use" tab in case there is anything in there that you need to know or look up. 

2. Then you would go to "Sensitivity Labels" tab.

    <img width="894" height="379" alt="Sensitivity Label Fill 1" src="https://github.com/user-attachments/assets/3c9e3a18-f108-433d-8465-bb344b5a36f1" /> <img width="1259" height="246" alt="Sensitivity Label Fill 2" src="https://github.com/user-attachments/assets/20d7a7f0-8d91-4439-a249-ff4c3c7eb27f" />
The Sensitivty Label Workbook

    <img width="1917" height="759" alt="Microsoft Purview Admin Center Label 1" src="https://github.com/user-attachments/assets/93d173ac-146e-4068-95a4-fcbce2808516" /> Microsoft Purview Sensitivity Label admin center

3. There are 3 fields in this tab that MUST BE FILLED OUT for the "Label" to be an option in other tabs. Othar than that you would fill out the rest of the fields in each label as needed and in the priority order you want. 

    - The 3 fields are "Label/ParentLabel/LabelGroup/Sub-Label:, "Name:", and "Scope:". 
    
    - In "Label/Parent Label/Label Group/Sub-Label:" your options are "Parent Label, Label Group, Label, and Sub Label.". A quick explanation and which to use are below. The options that you have to select for this to show in other tabs are "Labels and Sub Labels" since "Parent Labels and Label Groups" are containers for labels and not meant/don't have labels (Scopes).

        1. Label: This is a Label 
    
        2. Parent Label: This is the top label for the sub-labels, meaning it's the Label that the "Sub Labels" are nested under. Think of it like a label that you promote to a container but it's still a label which we call a "Parent Label" and it loses all its settings (Scopes) and should not be used from that point forward. If the label is not under a Parent Label it will be a label and if it is, it's a sub label.
    
        3. Label Group: This is going to be rolled out with modernization and will be replacing Parent Labels. It is like a true container and there will no longer be the concept of promoting a label to a parent label, there will only ever be containers and labels. Since this is a container, it will not have Label (Scopes.). If the label is not under a Label group it will be a label and if it is, it's a sub label.

        4. Sub Label: This is a label that is under/nested under a Parent Label/Label Group.

    - In the "Name" field all you need to do is fill in the name that will show in the admin center, this is different than the name that will show to end users which is "Display Name". 

    - Lastly, we have the "Scope" filled that must be filled out. Your options are "Files, & Other Data", "Emails", "Meetings", and "Groups & Sites". You can select all or none based on what functionality you need the Sensitivity Label to have. A quick explanation and which to use are below.

        1. Files, & Other Data: This must be selected if you want this label to be an option in the "Emails, Files, & Other Data". You can just select this and or "Emails" to have the label as an option in "Emails, Files, & Other Data" tab. Both "Files, & Other Data" and "Emails" must be selected for "Meetings" to be an option to select.

        2. Emails: This must be selected if you want this label to be an option in the "Emails, Files, & Other Data" tab. You can just select this and or "Files, & Other Data" to have the label as an option in "Emails, Files, & Other Data" tab. Both "Files, & Other Data" and "Emails" must be selected for "Meetings" to be an option to select.

        3. Meetings: This must be selected if you want this label to be an option in the "Teams meetings and chats" tab. 

        4. Groups & Sites: This must be selected if you want this label to be an option in the "Groups & Sites" tab.

        <img width="576" height="533" alt="Label dropdown example 1" src="https://github.com/user-attachments/assets/0ed7068c-16bd-4ba1-a7f7-feae2a77f88e" />

    - With everything filled out you will see the label show up in the appropriate tab like above. 

4. Then you would go to the appropriate tabs "Emails, Files, & Other Data", "Teams meetings and chats", and or "Groups & Sites" and fill out appropriate label settings. 

5. Then you can fill out the "Publishing" tab and plan out how you're going to push "Publish" labels to end users and the settings for it. 

6. Then you can fill out "Service-side Auto-Labeling" and or "Data Loss Prevention (DLP)" based on your plans to use the labels with them. 

## Applies To

- Microsoft Purview

## Author

|Author|Original Publish Date|Last Updated Date
|----|--------------------------|--------------
| Nicholas Bear | September 11, 2025 | September 15, 2025
| Thomas Reed | September 11, 2025 | September 15, 2025

## Issues

Please report any issues you find to the [issues list](https://github.com/NicholasBear-Tech/Bears-Tech/issues).

## Support Statement

The scripts, samples, and tools made available through the FastTrack Open Source initiative are provided as-is. These resources are developed in partnership with the community and do not represent official Microsoft software. As such, support is not available through premier or other Microsoft support channels. If you find an issue or have questions please reach out through the issues list and we'll do our best to assist, however there is no associated SLA.

## Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Legal Notices

Microsoft and any contributors grant you a license to the Microsoft documentation and other content in this repository under the [MIT License](https://opensource.org/licenses/MIT), see the [LICENSE](LICENSE) file, and grant you a license to any code in the repository under the [MIT License](https://opensource.org/licenses/MIT), see the [LICENSE-CODE](LICENSE-CODE) file.

Microsoft, Windows, Microsoft Azure and/or other Microsoft products and services referenced in the documentation may be either trademarks or registered trademarks of Microsoft in the United States and/or other countries. The licenses for this project do not grant you rights to use any Microsoft names, logos, or trademarks. Microsoft's general trademark guidelines can be found at http://go.microsoft.com/fwlink/?LinkID=254653.

Privacy information can be found at https://privacy.microsoft.com/en-us/

Microsoft and any contributors reserve all others rights, whether under their respective copyrights, patents,
or trademarks, whether by implication, estoppel or otherwise.
