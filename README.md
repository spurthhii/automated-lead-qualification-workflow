# Automated Lead Qualification Workflow

## Overview
This project demonstrates an automated lead qualification workflow that scores incoming leads based on predefined business rules and routes them into appropriate follow-up actions.

## Tools Used
- Google Sheets (CSV-based lead intake)
- Zapier (automation and routing)
- Gmail (email automation)
- Google Tasks (follow-up task creation)

## Lead Data Structure
Leads are stored in a CSV file with the following fields:
- Lead Name
- Email
- Industry
- Company Size
- Engagement Level
- Lead Score
- Lead Bucket
- Last Action Taken

## Lead Scoring Rules
Lead scores are calculated based on:
- Industry
- Company size
- Engagement level

### Scoring Logic
- Industry score + Company size score + Engagement score = Lead Score

### Lead Buckets
- Hot: Lead Score ≥ 50
- Warm: Lead Score between 30–49
- Cold: Lead Score < 30

## Email Triggers and Follow-Up Tasks

| Lead Bucket | Trigger Condition | Action Taken |
|------------|------------------|--------------|
| Hot | Lead Score ≥ 50 | Send demo/call email and create follow-up task |
| Warm | Lead Score 30–49 | Send nurture email |
| Cold | Lead Score < 30 | Send newsletter email |

## Workflow Summary
1. A new lead is added to the CSV file
2. Lead score is automatically calculated
3. Lead is assigned to a qualification bucket
4. Email and follow-up actions are triggered based on bucket

## How to Update Rules
- To update scoring rules, modify the lookup tables in Google Sheets
- To change email behavior, update Zapier paths
