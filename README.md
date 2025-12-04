# Maldives Business Registry Scraper
>This scraper collects detailed company information from the Maldives Business Registry based on search queries or exact matches. It retrieves registration data, shareholders, directors, activities, permits, and licenses in structured form. If you're researching companies, performing compliance checks, or enriching datasets, this tool gives you complete business profiles with minimal effort.

---

<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/Bitbash333" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>

<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong>Maldives Business Registry Scraper</strong> you've just found your team — Let's Chat. 👆👆
</p>

## Introduction
The Maldives Business Registry Scraper crawls registry search results and extracts full business details for each listed entity. It’s designed for analysts, researchers, compliance teams, and developers who need authoritative company information in a structured, consistent format.

### What It Helps You Do
- Look up registered Maldivian businesses by keyword or exact match.  
- Retrieve complete business profiles including ownership, governance, and activities.  
- Extract shareholder lists, directors, registration numbers, and SME classifications.  
- Build internal databases or automate due-diligence workflows.  
- Produce structured JSON output for seamless integration.

---
## Features
| Feature | Description |
|---------|-------------|
| Search & Exact Match Modes | Query the registry using flexible or strict matching. |
| Detailed Profile Extraction | Retrieves registration details, ownership, directors, and SME class. |
| Activities, Permits & Licenses | Extracts activity records, permit status, and licensing information. |
| Pagination Support | Collects results across multiple search pages. |
| Complete JSON Output | Produces rich structured objects for each business. |
| Error Handling | Handles missing fields gracefully and maintains consistent output. |

---
## What Data This Scraper Extracts
| Field Name | Field Description |
|------------|-------------------|
| business_id | Registry ID of the business. |
| detail_url | URL leading to the business detail page. |
| page_type | Indicates the content type (e.g., business detail). |
| extracted_at | Timestamp of extraction. |
| business_name | Legal name of the company. |
| business_type | Type of entity (Company, Partnership, etc.). |
| address | Registered address. |
| registration_number | Official registration reference. |
| status | Registration status. |
| upn | Unique profile number. |
| sme_classification | SME category (e.g., Small, Medium, Large). |
| owner | Owner information if available. |
| managing_director | Name of the managing director. |
| board_of_directors | List of directors with appointment dates. |
| board_of_directors_count | Count of board members. |
| shareholders | List of shareholders with join dates. |
| shareholders_count | Total number of shareholders. |
| business_names | Associated business names and registration details. |
| business_names_count | Count of registered business names. |
| business_activities | Activities, issue states, dates, and descriptions. |
| business_activities_count | Total number of activities. |
| permits | Permit-related info with status and details list. |
| licenses | License-related info with status and details list. |

---
## Example Output
    
    [
      {
        "business_id": "314159",
        "detail_url": "https://business.example.com/BusinessRegistry/ViewDetails/314159?key=271828",
        "page_type": "business_detail",
        "extracted_at": "2025-10-02T14:30:45.678901",
        "business_name": "THORNHILL INDUSTRIES Pvt Ltd",
        "business_type": "Company",
        "address": "H. SAMARITAN TOWER, 3rd FLOOR",
        "registration_number": "C04212021",
        "status": "Registered",
        "upn": "2021PV07742D",
        "sme_classification": "Large",
        "owner": null,
        "managing_director": "HAROLD FINCH",
        "board_of_directors": [
          {
            "name": "John Reese",
            "appointed_date": "10-Sep-2021"
          },
          {
            "name": "HAROLD FINCH",
            "appointed_date": "10-Sep-2021"
          }
        ],
        "board_of_directors_count": 2,
        "shareholders": [
          {
            "name": "John Reese",
            "join_date": "10-Sep-2021"
          },
          {
            "name": "Samantha Groves",
            "join_date": "10-Sep-2021"
          },
          {
            "name": "HAROLD FINCH",
            "join_date": "10-Sep-2021"
          }
        ],
        "shareholders_count": 3,
        "business_names": [
          {
            "name": "Northern Lights Solutions",
            "number": "BN98762025",
            "upn": "BN20250409999J"
          }
        ],
        "business_names_count": 4,
        "business_activities": [
          {
            "number": "BP56782023",
            "activity_description": "6201 Computer programming activities",
            "state": "Issued",
            "issued_date": "15-Mar-2030",
            "expiry_date": "",
            "business_name": "",
            "address": "M. Thornhill, Liberty Lane 67890, Metropolis, Example Nation"
          }
        ],
        "business_activities_count": 3,
        "permits": {
          "has_permits": false,
          "message": "Does not have any business permit owned by THORNHILL INDUSTRIES Pvt Ltd",
          "permits_list": []
        },
        "licenses": {
          "has_licenses": false,
          "message": "Does not have any business license owned by THORNHILL INDUSTRIES Pvt Ltd",
          "licenses_list": []
        }
      }
    ]

---
## Directory Structure Tree
    
    Maldives Business Registry Scraper/
    ├── src/
    │   ├── main.js
    │   ├── scraper/
    │   │   ├── search_client.js
    │   │   ├── detail_parser.js
    │   │   └── pagination_handler.js
    │   ├── utils/
    │   │   ├── normalize.js
    │   │   └── logger.js
    │   └── config/
    │       └── settings.example.json
    ├── data/
    │   ├── sample_input.json
    │   └── sample_output.json
    ├── package.json
    └── README.md

---
## Use Cases
- **Compliance teams** verify registrations and ownership structures before onboarding partners.  
- **Researchers** build datasets of Maldivian businesses for economic or market studies.  
- **Developers** integrate business lookup tools into internal systems.  
- **Financial institutions** automate KYC or risk assessments using structured registry data.  
- **Journalists** investigate corporate structures and entity relationships.  

---
## FAQs

**Can I filter results for exact matches only?**  
Yes, you can enable exact-match mode in the input options.

**Does it scrape full business profiles?**  
It returns detailed information including activities, shareholders, directors, and registration metadata.

**What happens if a field is missing?**  
Missing data is returned as null or an empty list, and the scraper continues smoothly.

**Can I use this for batch searches?**  
Yes, you can search for multiple business names or terms in one run.

---
### Performance Benchmarks and Results

**Primary Metric:**  
Extracts dozens of business profiles per minute depending on registry response times.

**Reliability Metric:**  
Maintains over 95% stability across large batch queries with consistent parsing patterns.

**Efficiency Metric:**  
Optimizes pagination and detail fetching to reduce redundant requests.

**Quality Metric:**  
Delivers highly structured, inspection-ready business records suitable for compliance and research workflows.


---


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/m-dRE1dj5-k?si=5kZNVlKsGUhg5Xtx" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review3.gif" alt="Review 3" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Exceptional results, clear communication, and flawless delivery. <br>Bitbash nailed it."
      </p>
      <p style="margin:1px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
         </p>

