# NHS Country Directors Patient Care Activity Storyboard: Driving Strategic Healthcare Decisions

## Overview

This project presents a comprehensive Tableau storyboard designed specifically for NHS Country Directors, offering an executive overview of patient care activity across England. It aims to provide a high-level, yet insightful, narrative of patient journeys, service utilization, and key performance indicators (KPIs) across different regions and care settings. Its interactive design allows for a guided exploration of data to support strategic decision-making and operational planning for enhanced patient care.

## Why This Project is Relevant

For healthcare leaders like NHS Country Directors, having a clear and immediate understanding of patient care activity is crucial for effective resource allocation, policy implementation, and service improvement. This storyboard is highly relevant because it:

Facilitates Strategic Oversight: Provides a consolidated view of critical patient care metrics, enabling directors to monitor the health and efficiency of services under their purview. This includes record-high activity at 21.5 million consultant episodes alongside persistent waiting lists of 7.5 million and declining 18-week performance.

Informs Resource Allocation: Helps identify areas of high demand or resource strain, guiding decisions on where to deploy staff, equipment, or funding, particularly in areas with "long-tail" waiting lists or high bed occupancy.

Supports Policy Development: Offers data-driven insights into patient pathways and outcomes, aiding in the development of more effective healthcare policies, such as targeted interventions for specific specialties or regions.

Enhances Accountability: Enables easy tracking of performance against constitutional standards (e.g., 92% 18-week target) and international benchmarks (OECD median waiting times), fostering transparency and accountability.

Streamlines Communication: Presents complex data in an intuitive and narrative-driven format, making it easier to communicate insights to diverse stakeholders, from operational managers to political leaders.

## Research Objectives

This storyboard was developed to achieve the following key objectives for NHS Country Directors:

To provide an executive-level overview of patient care activity and trends, contextualizing challenges like high bed occupancy (93%) and long waiting lists.

To highlight key patient journeys and service utilization patterns, including elective vs. emergency case mix and patient flows between Integrated Care Boards (ICBs).

To enable comparison of patient care metrics across different geographical areas or service lines, identifying regional disparities and high-pressure specialties.

To support data-driven discussions and strategic planning regarding patient care capacity and quality, drawing on insights from domestic performance and international comparisons.

To offer a guided narrative through relevant data points, simplifying complex healthcare information to facilitate rapid pattern recognition and drill-through accountability.

## Methodology

This project leverages Tableau's interactive visualization capabilities to present a "storyboard" of patient care activity. The methodology focuses on clear data presentation and a narrative flow to guide users through key insights, from high-level overviews to specific actionable details.

## Data Sources and Features

Datasets were taken from: Hospital Admitted Patient Care Activity, 2023-24 (https://digital.nhs.uk/data-and-information/publications/statistical/hospital-admitted-patient-care-activity/2023-24) and OECD Median Waiting Time series (2014-2023).

Patient Activity Data: Records of 21.5 million finished consultant episodes, 17.6 million first attendances, and 53.9 million bed-days, along with diagnostic (ICD-10) and procedure (OPCS) codes.

Demographic Data: Patient age and gender (e.g., revealing 15% higher female activity rates).

Service Metrics: Data on waiting times (e.g., 7.5 million pathways on waiting lists, 57% 18-week performance), length of stay, and finished consultant episodes.

Operational Data: Information on hospital bed occupancy (e.g., 93% general and acute bed occupancy).

External Benchmarking Data: OECD median waiting times for specific procedures (e.g., joint replacement, cataracts) to contextualize England's performance internationally.

## Key features derived from such data include:

Number of admissions/discharges over time: Tracking overall patient demand.

Patient flow through different care pathways: Analyzing inflow/outflow dynamics between ICBs and provider trusts.

Utilization rates of specific services or departments: Highlighting busy areas and capacity strains.

Regional performance metrics for various patient care activities: Comparing ICB and trust-level performance on waiting times and activity.

Case-mix analysis: Understanding the balance of elective vs. emergency cases by region.

## Data Pre-processing

Standard data pre-processing steps were crucial for ensuring the quality and usability of this complex healthcare data:

Data Extraction: Collecting relevant data from NHS Hospital Episode Statistics and OECD API.

Data Cleaning: Employing Excel Power Query for initial operations, including header banner removal, converting suppression markers to null values, and transforming text percentages to floating-point format. Data integrity was ensured by Official Statistics designation and completeness rates exceeding 99%.

Data Anonymization/Pseudonymization: Handled at the source by NHS Digital to ensure patient privacy and compliance.

Data Transformation: Aggregating granular data and establishing relationships within Tableau due to substantial size and complex key relationships across nine Hospital Patient Care tables. This involved standardizing key fields (icb_code, provider_code, icd10_code, opcs_code, financial_year).

Categorization: Executing self-joins on Provider-Level Analysis to capture both origin and treatment ICBs for inflow-outflow analysis, and left joins with OECD data using procedure codes and year bucket fields to align reporting calendars.

Output: Generating six discrete cleaned extracts (a central fact table and five dimensional supplements) rather than a consolidated file, optimizing performance.

## Data Processing/Analysis/Methods Used

The primary methods employed are Data Visualization and Interactive Storytelling within Tableau, ensuring a guided narrative flow that guides users through key insights.

Time Series Analysis: Using line charts and area charts to illustrate trends in patient admissions, discharges, and activity over time.

Geographical Mapping: Employing compact OECD maps to position England's waiting times internationally and implicitly through regional breakdowns in domestic dashboards.

Key Performance Indicators (KPIs): Prominently displaying critical metrics such as finished consultant episodes, waiting list pathways, and 18-week performance.

Bar Charts/Treemaps: Visualizing activity breakdown by service type, patient demographics (e.g., gender-stratified bars), or care pathway stages (e.g., elective vs. emergency case mix). Procedure group treemaps offer immediate part-to-whole context.

Advanced Chart Types:

Median-versus-Mean Scatter Plots: Used to expose "long-tail" integrated care boards with extreme waiting times.

Dual-Axis Scatter Plots: Correlating planned versus emergency workload by specialty, sized by mean waiting times, to expose high-throughput, high-delay specialties like Orthopaedics.

Bubble Charts: Ranking ICD-10 categories to identify clinical demand patterns (e.g., musculoskeletal trauma).

Storyboarding: Organizing a sequence of dashboards into a guided narrative flow (Executive Overview, Access and Backlog, Capacity and Utilization, Clinical Demand and Benchmark) allowing Country Directors to follow a logical progression of insights.

Filtering and Interactivity: Implementing global filters and action filters (e.g., one-click highlighting actions connecting scatter points to waiting list rankings) to allow users to drill down into specific periods, regions, or patient cohorts without database re-querying, preserving performance.

## Technologies Used

Tableau Public: The platform used for developing and sharing the interactive storyboard dashboard, leveraging its logical layer for efficient data relationships and referential integrity.

Microsoft Excel: Used for initial raw data storage, cleansing, and aggregation using Power Query before being connected to Tableau.

## Key Findings

While specific findings require interaction with the live dashboard, this project aims to highlight:

Overall Patient Activity Trends: Visualizing record-high activity (21.5 million consultant episodes) contrasting with persistent waiting lists (7.5 million pathways) and declining 18-week performance (57%).

Regional Disparities and "Long-Tail" Delays: Identifying specific ICBs (e.g., Midland’s regions, Devon, Kent & Medway, North-West London) with significant "long-tail" distributions in elective waits, collectively accounting for over 25% of 52-week breaches.

Capacity Constraints & Utilization: Demonstrating that general and acute bed occupancy has reached 93%, deemed unsafe. Insights into patient flow show London trusts as substantial net importers, straining local bed capacity.

Clinical Demand Hotspots: Pinpointing Orthopaedics as a critical "pressure specialty" with high volume, mixed emergency-elective demand, and the longest waiting times.

International Performance Gaps: Benchmarking reveals England's significant underperformance in joint replacement and cataract procedures relative to OECD peers like Denmark and Portugal, who achieve sub-70-day medians.

## Recommendations

Based on the types of insights the dashboard provides, the project culminates in five actionable recommendations for NHS Country Directors:

Targeting Long-Tail ICBs: Directing interventions to specific regions identified with disproportionately long waiting lists.

Expanding Bed Capacity: Including scaling virtual wards from 8,241 to a projected 15,000 beds by 2025.

Accelerating Long-Term Workforce Plan Implementation: Doubling medical school places to 15,000 by 2031 to address staffing needs.

Focusing Resources on High-Delay Specialties: Particularly Orthopaedics, to reduce the most significant bottlenecks.

Policy Review and Benchmarking: Using international comparisons to inform adjustments to existing healthcare policies and establish clear improvement targets.



## How to View the Dashboard

The interactive storyboard dashboard is publicly available on Tableau Public.
You can access and interact with the dashboard here:

🌐 NHS Country Directors Patient Care Activity Storyboard on Tableau Public
