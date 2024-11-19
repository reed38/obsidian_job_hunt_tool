# Obsidian Job Application Tracker

## Why This Was Created

During my internship search, I found traditional methods like spreadsheets inadequate for managing multiple applications, interview notes, and company research. I needed a system that could:

- Track application statuses effectively
- Store detailed interview notes
- Organize company research
- Provide quick overview of progress

This Obsidian-based system solves these challenges by offering:

- Templates for rapid application and company note creation
- Linked notes connecting applications, companies, and interview details
- Automated status dashboard using Dataview
- Rich text formatting for comprehensive note-taking
- Quick access to all application-related information in one place

## File Structure
```bash
.
├── Companies/     # Company profiles from template
├── Offers/       # Applications from template, links to companies
├── _template/    # Templates for consistent data structure
├── Dashboard.md  # Auto-updating status overview
└── README.md
```

## Template System
Templates use inline fields: [**tag_name**::value_type]
Value types:
- string: Text
- int: Numbers
- date: Dates
- boolean: true/false
- obsidian_link: Links to other notes

## Job Offer Template Contents
- Basic Information: company, title, sector, location
- Contact Details: name, phone, email
- Application Status: applied, interview stages, rejection
- Offer Details: remuneration, advantages
- Documentation section for notes

**Note:** Some status fields are set to false by default at creation to not have to manually change them at each note creation (ex: second_interview_passed  tag will never be set to true when the application starts.

## Company Template Contents
- Company Profile: name, type, sector, location
- Contact Information
- Company Overview: mission, products, clients
- Size: revenue, employees
- Additional Information: news, history, awards

## Dashboard
Shows:
- To apply
- Pending responses
- Interview stages
- Rejected/Withdrawn

## Setup
1. Clone repository
2. Open as Obsidian vault
3. Enable plugins
4. Create notes from templates
5. Track in Dashboard

**Note**: Sample applications and company descriptions are included in this repository as examples of the system in use.