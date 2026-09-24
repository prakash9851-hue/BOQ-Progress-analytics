Rail Project Cost Estimation & Progress Analytics

Two small tools that replace manual spreadsheet work on a railway siding project: a web-based BOQ Builder that estimates earthwork and track quantities and costs, and an Excel progress tracker that turns daily site quantities into progress and balance-quantity reports.

All data in this repository is dummy data. Quantities, rates, names and dates are invented for demonstration. No company, contractor or site data is included.

Live demo (BOQ Builder): https://prakash9851-hue.github.io/rail-boq-progress-analytics/

Show Image

Why I built this

While working on a railway siding project, I saw two recurring problems:

Estimates went out of date quickly. Site conditions kept changing, so early BOQ quantities changed too, which delayed material procurement decisions.
Progress reporting was manual. Daily quantities were collected in fragmented formats, so it was hard to see how far each activity had actually progressed.

These tools aim to make estimating faster and progress visible at a glance.

Tool 1: PWAY BOQ Builder (index.html)

A single-page web app that generates a Bill of Quantities for permanent-way (track) works.

Inputs

Section type: cutting or embankment
Formation width (w1) and height/depth (h)
Total cutting and filling volume (m³)
Track kilometres (TKM) and number of lines
Turnout details: crossovers (1 in 12, 1 in 8.5), dead ends, derailing switches

What it does

Builds an itemised BOQ from the inputs
Applies either a sample 2024 rate schedule or your own rates
Shows a cost distribution chart so the biggest cost items are visible
Exports the final BOQ to Excel

How to use

Open the live demo (or open index.html in a browser; internet is needed to load the chart and Excel libraries).
Select the section type and enter the dimensions and volumes.
Choose how rates should be applied.
Click Generate Final BOQ, then Download Excel BOQ.
Tool 2: Excel Progress Tracker (excel/Progress_Tracker_Demo.xlsx)

A daily progress report workbook that compares executed quantities against total scope.

Sheet	Covers
Common_Report	Consolidated daily progress across all domains
CV1_ROB	Bridges, culverts and road-over-bridge items
CV2_Infra	Station building and infrastructure items
CV3_Pway	Blanketing, ballasting, sleepers, track linking, points & crossings
Earthwork	Earthwork quantities by land category

What it does

Tracks scope, cumulative executed quantity, balance quantity and progress % for each item
Uses weighted averages (from excavation to RCC) so progress reflects the size of each activity
Consolidates 40+ activity metrics into a single report view for daily monitoring
Tech stack
BOQ Builder: HTML, CSS, JavaScript, Chart.js, SheetJS
Progress Tracker: Microsoft Excel (formulas, conditional formatting, dashboard view)
Repository structure
rail-boq-progress-analytics/
├── index.html                          # BOQ Builder (live demo)
├── excel/
│   └── Progress_Tracker_Demo.xlsx      # Progress tracker (dummy data)
├── screenshots/                        # Images used in this README
└── README.md
Possible improvements
Power BI dashboard for real-time project monitoring
Single platform linking planning, procurement and execution
Scheduling module that estimates time per activity and forecasts completion date
Author

Prakash Gupta B.Tech, Civil Engineering, IIT (ISM) Dhanbad GitHub | LinkedIn

Disclaimer

These tools are for learning and demonstration. Rates and quantities are illustrative, so verify them against current schedules and project data before any real use.
