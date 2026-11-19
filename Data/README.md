# BGSO Resource Map – Recreated Dataset

This repository holds a recreated version of the data behind the **BGSO Resource Map**. The map is a hand-drawn-style visualization of the people, offices, trainings, and partner organizations that new leaders of Carnegie Mellon University's Black Graduate Student Organization (BGSO) should connect with, in the recommended order.

## Why this is a recreated dataset

The original data comes from BGSO's internal records (transition notes, meeting minutes, contact lists, event and budget records). Those records are stored privately in the BGSO Google Drive and on the author's laptop. They include member information and personal contact details, so they are not posted publicly. This file keeps only public-facing role information, with no member data and no personal emails or phone numbers. Where a contact is listed, it is a public office address.

## Files

| File | Description |
|---|---|
| `bgso_resource_map.csv` | One row per resource (person, office, training, or partner organization) shown on the map |
| `bgso_money_map.csv` | One row per income source or expense shown on the money map (2026–27). `status` marks money as `confirmed`, `spent`, or `goal (pending)` |

## Columns

| Column | Description |
|---|---|
| `step` | Order in the recommended course of action (1–5 = sequential steps on the "brick road"; 6 = ongoing peer network) |
| `resource_id` | Unique ID for each row |
| `name` | Person, training, or organization name |
| `role` | Role or description |
| `affiliation` | Office, association, or platform the resource belongs to |
| `category` | `advisor`, `training`, `funding`, or `peer organization` |
| `priority` | `primary` (main contact for that step), `secondary` (additional contact), or `ongoing` (relationship to maintain) |
| `map_element` | How the row appears on the map: `gold star`, `gold star (sub-contact)`, or `hub satellite` |
| `contact_method` | How to reach the resource (public channels only) |
| `academic_year` | Year the information applies to |
| `source` | Where the information came from |
| `source_url` | Public link to the source, where one exists |

## How the data maps to the visualization

- Rows with `step` 1–5 are drawn as gold stars along a yellow-brick-road path, in step order.
- Sub-contacts (for example, new CMBAA advisors) are listed under their step's star.
- Rows with `step` 6 are drawn as satellites around a "Club Leads Network" hub, reached by a looping path to show relationships that continue over time.

## Public sources

- CMU Office of Student Involvement and Traditions – Forms and Meeting Requests: https://www.cmu.edu/student-affairs/sit/student-org-resources/forms.html#finance
- CMU Student Org Financial Resources: https://www.cmu.edu/student-affairs/sit/student-org-resources/financial/index.html
- CMU Student Government – JFC Funding: https://www.cmu.edu/stugov/sbvpf/funding.html
- CMU Institutional Research and Analysis – Common Data Set (graduate enrollment context): https://www.cmu.edu/ira/

## Notes

- Information is current for the 2026–27 academic year. Advisors and club leads change, so check each contact before relying on it.
- Club leads are listed by organization only. Current leads' names are kept in BGSO's private records.
