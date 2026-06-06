## KPI Performance Management System

<img width="2050" height="1206" alt="Screenshot 2026-06-06 at 17 15 48" src="https://github.com/user-attachments/assets/a050a3ed-15d7-47a8-bbc4-bded19ae7a6a" />


# Overview

The KPI Performance Management System is a Power Platform solution designed to digitally manage employee daily task planning, execution tracking, compliance monitoring, behavioral assessments, and performance reporting across the organization.

The application enables employees to plan their daily work, update progress throughout the day, submit completion reports, and measure performance against defined productivity and compliance metrics.

The solution provides visibility for Employees, Heads of Department (HODs), Management, and Administrators through role-based dashboards and automated workflows.

⸻

# Objectives

* Digitize daily task planning and reporting.
* Improve accountability and transparency.
* Measure employee productivity and compliance.
* Provide behavioral assessment and performance insights.
* Enable management oversight and intervention where necessary.
* Reduce manual reporting and paper-based processes.

⸻

# Technology Stack

**Frontend**

* Microsoft Power Apps (Canvas App)

**Backend**

* SharePoint Online Lists or Dataverse Table

**Automation**

* Microsoft Power Automate

**Identity**

* Microsoft Entra ID (Azure Active Directory)

⸻

## User Roles

Employee

Employees can:

* Create daily tasks.
* Add task line items.
* Update task progress throughout the day.
* Submit task completion reports.
* View personal performance metrics.
* View historical task submissions.
* View behavioral assessment scores.

⸻

## Head of Department (HOD)

HODs can:

* View employees within their department.
* Review employee performance metrics.
* View departmental performance.
* View behavioral assessments.
* Monitor productivity trends.
* Receive management observations and concerns.
* Review flagged task repetition cases.

⸻

## Management

Management can:

* Monitor employee performance across departments.
* Review compliance and behavioral trends.
* Raise observations against employees.
* Escalate concerns to HODs.
* Review organizational KPI performance.

⸻

## System Administrator

Administrators can:

* Manage employee records.
* Manage departments.
* Manage HOD assignments.
* Maintain KPI configuration.
* Access Employee Management dashboard.

⸻

## SharePoint Lists or Dataverse Table

# Employee Master Template

Stores employee information.

Key Columns

* Employee Name
* Email
* Department
* Role
* Reporting Manager
* HOD

⸻

# Task_List

Stores daily task header records.

Key Columns

* TaskID
* EmployeeName
* EmployeeEmail
* Department
* WeekNumber
* ComplianceScore
* DailyProductivityScore
* FinalComplianceScore
* ReportTime
* Status

⸻

# Task_List_Item

Stores task line items.

Key Columns

* TaskGUID
* Task_Entry_Details
* Closing_Report
* Task_Status
* Task_Weight
* Entry_Time

⸻

# Behavioral_Review

Stores weekly behavioral assessments.

Key Columns

* EmployeeName
* EmployeeEmail
* Department
* WeekNumber
* BehavioralScore
* BehavioralScoreValue
* HODEmail
* Status

⸻

# HOD_List

Stores departmental HOD assignments.

Key Columns

* Department
* HODName
* HODEmail

⸻

# KPI_App_Admin

Stores administrator accounts.

Key Columns

* Email

⸻

Employee Task Management

Create Daily Task

Employees create a daily task record.

Compliance Scoring

Employees receive:

* 50 points when task is created before 8:00 AM.
* 0 points when task is created after 8:00 AM.

⸻

Task Line Items

Employees can:

* Add multiple task entries.
* Assign task weights.
* Update task progress throughout the day.
* Add closing reports.

⸻

Task Statuses

Task Progress Score Legend

Task Status	Score
Not Started	0
Initial Work Started	40
Work In Progress	60
Near Completion	80
Completed	100
Cancelled	Excluded

Cancelled tasks do not contribute to productivity calculations.

⸻

Closing Reports

Employees are required to provide a Closing Report for all active tasks before closing their daily task submission.

The Closing Report captures:

* Work completed.
* Progress achieved.
* Outcomes delivered.
* Additional remarks.

⸻

Productivity Scoring

Daily Productivity Score

Daily Productivity Score is calculated using task progress scores.

Formula

Daily Productivity Score =

Average of all active Task Progress Scores

Example

Task	Status	Score
Task A	Completed	100
Task B	Work In Progress	60
Task C	Near Completion	80

Result:

(100 + 60 + 80) ÷ 3 = 80%

⸻

Compliance Scoring

Morning Submission Score

Condition	Score
Created before 8:00 AM	50
Created after 8:00 AM	0

⸻

End-of-Day Submission Score

Condition	Score
Closed before 6:00 PM	50
Closed after 6:00 PM	0

⸻

Compliance Score

Scenario	Score
Created before 8AM and closed before 6PM	100
Created before 8AM and closed after 6PM	50
Created after 8AM and closed before 6PM	50
Created after 8AM and closed after 6PM	0

⸻

Final Compliance Score

The Final Compliance Score combines productivity and compliance.

Formula

Final Compliance Score =

(Daily Productivity Score + Compliance Score) ÷ 2

Example

Compliance Score = 100

Daily Productivity Score = 80

Final Compliance Score =

(100 + 80) ÷ 2

= 90%

⸻

Behavioral Review Process

Weekly Review

Every employee receives a weekly behavioral assessment.

Behavioral reviews are generated automatically based on weekly performance data.

⸻

Behavioral Score Legend

Rating	Score
Excellent	100
Good	80
Average	60
Poor	40
Very Poor	20

⸻

# HOD Dashboard

The HOD Dashboard provides:

Department Overview

* Department Compliance Score
* Department Behavioral Score
* Employee Count
* Performance Trends

⸻

# Employee Insights

HODs can view:

* Employee Tasks
* Behavioral Reviews
* Compliance Scores
* Productivity Scores
* Weekly Performance Trends

⸻

# Management Observation Feature

Management can raise observations against any employee.

The process allows:

1. Selecting an employee.
2. Entering an observation or concern.
3. Automatically notifying the employee’s HOD.
4. Requesting HOD review and feedback.

This feature improves accountability and management oversight.

⸻

# Employee Performance Dashboard

Employees can view:

Compliance Metrics

* Compliance Score
* Productivity Score
* Final Compliance Score

⸻

Behavioral Metrics

* Weekly Behavioral Scores
* Behavioral Trends

⸻

Historical Performance

* Task History
* Weekly Reviews
* Performance Charts

⸻

# Security Model

Access is controlled using Microsoft Entra ID and SharePoint permissions.

Employees

Can only view their own performance records.

HODs

Can view employees assigned to their department.

Administrators

Can access Employee Management functionality.

Management

Can review performance across departments and submit observations.

⸻

# Notifications

The system sends automated notifications for:

* Management observations.
* Behavioral reviews.
* HOD actions.
* Employee feedback requests.
* Performance escalations.

⸻

# Future Enhancements

Planned enhancements include:

* AI-powered task repetition analysis.
* Power BI integration.
* Mobile-first experience.
* Advanced analytics and forecasting.

⸻

Benefits

* Improved employee accountability.
* Increased operational transparency.
* Consistent performance measurement.
* Faster managerial intervention.
* Data-driven decision making.
* Reduced manual reporting.
* Improved organizational productivity.
