# Data Licensing

The data product may be exploited e.g. by licensing its use and exploitation to third parties. Machine-readable license as part of the specification is implemented for this purpose. It can be used to conclude various agreements regarding data protection, processing and intellectual property rights (IPR). Data can be protected by one or more intellectual property rights. Principle is that when a third party (Data User) exploits the data, it must have a license or other right from Data Holder to exploit to the data.

> Example of License Object usage:


```javascript
  
"license": {
   "scope": {
         "definition": "The purpose of this license is to determine the terms and conditions applicable to the licensing of the data product, whereby Data Holder grants Data User the right to use the data.",
         "language": "en-us",
         "restrictions": "Data User agrees not to, directly or indirectly, participate in the unauthorized use, disclosure or conversion of any confidential information.",      
         "geographicalArea": [ 
            "EU",
            "US"
         ]
         },
   "LicenseLimitations": [ 
          "Permanent",
          "Exclusivity",
          "Reproduction",
          "Display",
          "Distribution",
          "Adaptation",
          "Resellable",
          "Transferable",
          "Sublicensable"
         ],
   "privavcy": {
         "containsPersonalData": true,
         "applicaplePrivacyLaws": [ 
            "General Data Protection Regulation",
            "Personal Information Protection and Electronic Documents Act (PIPEDA)",
            "California Consumer Privacy Act (CCPA)"
         ],
         "dpaURL": "http://192.168.10.1/dpaconditions",
         },
   "termination": {
         "terminationContitions": "Cancellation before 30 days. After the expiry of the right of use, the product and its derivatives must be removed.",
         "continuityConditions": "Expired license will automatically continued without written cancellation (termination) by Data Holder",
         "forceMajeure": "Each party may suspend the fulfilment of its contractual obligations, when the said fulfilment is impossible or objectively too costly due to an unforeseeable impediment independent from the parties, such as for example: strike, boycott, lockout, fire, war (declared or not), civil war, riots and revolutions, requisitions, embargo, power blackouts, extraordinary breakage of machinery, delays in the delivery of components or raw materials."
         },
   "governance" : {
         "damages": "During the term of license, except for the force majeure or the Data Holders reasons, Data User is required to follow strictly in accordance with the license. If Data User wants to terminate the license early, it needs to pay a certain amount of liquidated damages.",
         "confidentiality": "Data User undertakes to maintain confidentiality as regards all information of a technical (such as, by way of a non-limiting example, drawings, tables, documentation, formulas and correspondence) and commercial nature (including contractual conditions, prices, payment conditions) gained during the performance of this license." 
         "applicableLaws": "This license shall be interpreted, construed and enforced in accordance with the law of Finland, Incl. Copyright Act 404/1961."
         "warranties": "Data Holder makes no warranties, express or implied, guarantees or conditions with respect to your use of the data product. To the extent permitted under local law, Data Holder disclaims all liability for any damages or losses, including direct, consequential, special, indirect, incidental or punitive, resulting from Data User use of the data product.",
         "audit": "Data Holder will reasonably cooperate with Data User by providing available additional information concerning the data product. Each party will bear its own costs with respect to the audit procedures."
         }
  }

  
```
| <div style="width:150px">Element name</div>   | Type  | Options  | Description  |
|---|---|---|---|
| scope | element | - |  Extent, range, coverage, area or space of the license. |
| definition | string | text content, max length 512 chars  | Background and purpose of the license. |
| language | string | ISO 639-1 standard language codes | License language. |
| permanent | boolean | true/false|  License with no expiration date. |
| termination | element | - | Licence termination and continuity related condititions. |
| terminationConditions | string | text content, max length 512 chars | Cancellation conditions of the license. |
| continuityConditions | string |  text content, max length 512 chars | Continuity conditions of the license. |
| restrictions | string | text content, max length 512 chars  | Restrictions of the license. |
| geographicalArea | string |  ISO 3166-1 alpha-2 codes | License right restricted to the geographical area. |
| licenseLimitations| array |  Options: Reproduction, Display, Distribution, Adaptation (right for derivate work), Resellable, Transferable, Sublicensable | Limited rights by the licence. Licenses can by default be assigned, transferred or sublicensed to another party, unless it is specifically restricted in the license agreement. |
| governance | element | - | Governance is the approach taken to ensure that the agreed outcomes are being fulfilled. |
| privacy | element | - | Data privacy related attributes. |
| containsPersonalData | boolean | true/false | Data contains personal data. |
| applicaplePrivacyLaws| array| oneOf: listed laws from the UNCTAD maintained tool, https://unctad.org/page/data-protection-and-privacy-legislation-worldwide | The Privacy Law frameworks which are covered. Many of us know about The California Consumer Privacy Act of 2018 (CCPA) and  General Data Protection Regulation (GDPR) but the those are just the tip of the iceberg. 137 out of 194 countries had put in place legislation to secure the protection of data and privacy. (21st Feb 2023) |
| dpaURL| URL| valid URL | The URL of the Data Processing Agreement (DPA). |
| audit | string | text content, max length 512 chars | License auditing terms. |
| warranties | string | text content, max length 512 chars | License warranties. |
| forceMajeure | string | text content, max length 512 chars | Force Majeure |
| damages| string | text content, max length 512 chars | Damages refers to the sum of money (i.e. indemnifications) for a breach of some duty or violation of license right. |
| confidentiality | string | text content, max length 512 chars| Restrictions and requirements imposed on the Data User regarding e.g. the use and disclosure of the Data Holder's confidential information. |
| applicableLaws | string | text content, max length 512 chars | Applicable laws not covered in **applicaplePrivacyLaws**, i.e local acts, degrees or law. |
