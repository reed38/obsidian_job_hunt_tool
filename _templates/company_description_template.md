# Obsidian Job Application Tracker

## Why This Was Created
During my internship search, I needed a system beyond spreadsheets. The key features:
- Templates for quick creation of application and company notes
- Connected information between applications and companies
- Rich text for interview notes
- Automated status tracking via dashboard
- Document linking
## File Structure
```bash
.
├── Companies/     # Company profiles
                  # - Contains research, company info
                  # - Created from company template
                  # - Links to related applications
                  
├── Offers/       # Job applications
                  # - One note per application
                  # - Created from offer template
                  # - Tracks status, interviews, contacts
                  # - Links to company profile
                  
├── _template/    # Template files
                  # - Offer template: quick application creation
                  # - Company template: standardized company info
                  # - Ensures consistent data structure
                  # - Default values set for application stages
                  
├── Dashboard.md  # Status overview
                  # - Auto-updates via Dataview
                  # - Shows all applications by stage
                  # - Links to application details
└── README.md
```

## Prerequisites
- Templates (core plugin)
- Dataview plugin

## Templates

### Job Offer Template
```markdown
## Basic Information
[**company**::obsidianLink]
[**offer_title**::string]
[**expertise_sector**::string]
[**location**::string]

## Contact Details
[**contact_name**::string]
[**contact_phone**::string]
[**contact_mail**::string]

## Application Status
[**applied**::true]
[**application_date**::date]
[**first_interview_planned**::false]
[**first_interview_passed**::false]
[**second_interview_planned**::false]
[**second_interview_passed**::false]
[**rejected**::false]
[**abandonment**::false]
[**reasons_abandonment**::string]

## Offer Details
[**remuneration**::int]
[**others_advantages**::string]

## Documentation
[Job Description](link)
```

Note: Status fields default to false as they represent stages not yet reached in a new application.

### Company Template
```markdown
# Company Description
## Company Profile
[**name**::string]
[**company_type**::string]
[**industry_sector**::List[string]]
[**location**::string]
[**website**::string]
[**contact_name**::string]
[**contact_phone**::string]
[**contact_mail**::string]

## Overview
- Mission description
- Products/Services
- Key Clients
- Competitors

## Size
[**revenues**::string]
[**employees_number**::string]

## Additional Information
- Recent News
- Social Media
- History
- Awards
```

## Dashboard
Uses Dataview queries to show:
- Applications to submit
- Pending responses
- Interview stages
- Rejected applications
- Withdrawn applications

## Setup
1. Clone repository
2. Open as Obsidian vault
3. Enable required plugins
4. Use templates to create notes
5. View progress in Dashboard

Would you like any section expanded?