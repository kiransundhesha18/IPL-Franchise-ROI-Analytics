# IPL-Franchise-ROI-Analytics

IPL Franchise Valuation & Player ROI
Project Documentation & Architecture
1. Project Overview
This project is an interactive, "Moneyball"-style sports analytics dashboard built in Power BI. It evaluates
the financial efficiency of Indian Premier League (IPL) franchises by comparing a player's auction
acquisition cost against their actual on-field performance (runs scored and wickets taken). The dashboard
serves as a comprehensive tool for analyzing squad building strategies and tracking capital allocation
efficiency.
2. Business Problem & Objective
During the IPL auction, franchises spend massive budgets (totaling upwards of ₹1,192 Crores across the
league) to build competitive squads. However, high auction prices do not always guarantee high
performance, frequently leading to inefficient capital allocation.
The primary objective of this dashboard is to move beyond traditional cricket statistics and accurately
measure Financial Return on Investment (ROI). It enables team management, scouts, and data analysts
to:
Identify Draft Steals: Pinpoint undervalued players who provide high output at a low acquisition cost.
Expose Inefficiencies: Highlight expensive underperformers who consume large portions of the salary
cap with minimal on-field contribution.
Audit Franchise Strategy: Evaluate aggregate spending efficiency at the team level to inform future
auction bidding strategies.
3. Analytical Methodology
To accurately measure financial efficiency, the data model normalizes player valuation by isolating specific
roles. Evaluating a pure bowler based on runs scored creates skewed, inaccurate data. Therefore, the
architecture relies on context-specific DAX (Data Analysis Expressions) measures engineered directly into
the Power BI semantic model.
By dividing monetary spend by distinct performance units, the model creates an equitable baseline to
compare players across different price tiers and franchise rosters.
Custom DAX Engineering
Cost_Per_Run_₹ : Evaluates Batters and All-rounders by dividing their total auction price by
total runs scored. Identifies the true cost of batting output.
Cost_Per_Wicket_₹ : Evaluates Bowlers and All-rounders by dividing their total auction price
by total wickets taken. Normalizes bowling efficiency independent of batting expectations.
4. Dashboard Features & Functionality
The dashboard provides a top-down executive view that seamlessly drills down into individual player
analytics via interconnected visuals.
Interactive Tile Navigation: Users can filter the entire dashboard architecture by selecting specific
Franchise tiles (e.g., Chennai Super Kings, Mumbai Indians) or Player Roles (Batter, Bowler, All-rounder,
Wicketkeeper) using clean, app-style slicers.
Dynamic KPI Scorecard: A centralized metric ribbon displays real-time, responsive calculations for
Total Spend (₹ Cr), Total Runs, and Total Wickets based strictly on the selected franchise or player role.
Dual-Pillar ROI Scatter Plots:
Batting ROI (Price vs. Runs): Maps batters across a quadrant to instantly visualize high-performing
bargains (bottom-right) versus costly investments (top-left).
Bowling ROI (Price vs. Wickets): Mirrors the batting visual to map bowling efficiency, guaranteeing
pure bowlers are correctly assessed on their primary skill.
Performance Matrix: A comprehensive data table providing granular, player-by-player breakdowns of
aggregate output and exact monetary cost per unit of performance.
5. Technical Stack
Platform: Microsoft Power BI Desktop
Data Engineering & ETL: Power Query (Data type validation, handling nulls, formatting)
Calculations: DAX (Data Analysis Expressions) for custom ROI metrics
UI/UX Design: Dark-theme executive layout, dynamic conditional filtering, classic KPI scorecards
