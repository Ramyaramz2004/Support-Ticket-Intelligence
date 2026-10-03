# Customer Support Ticket Priority Prediction and Automation

An intelligent, end-to-end customer support automation solution built using **Salesforce**, **Agentforce**, and custom data flows to streamline ticket management, predict priority levels, and automate agent assignments.

## 🚀 Project Overview
Managing customer support tickets efficiently is critical for maintaining high service-level agreements (SLAs). This project leverages Salesforce custom objects, auto-launched flows, and Agentforce subagents to analyze incoming support issues, determine their urgency, and surface structured ticket insights directly through natural language queries.

## 🛠️ Key Components & Architecture
* **Custom Object**: `Support Ticket Intelligence` (`Support_Ticket_Intelligence__c`)
  * **Auto Number Record Name**: `Ticket Number` (Format: `TKT-{0000}`)
  * **Key Fields**: Customer (Account Lookup), Contact (Contact Lookup), Issue Type (Picklist), Description (Long Text Area), Priority Level (Picklist), Status (Picklist), Created Date, Assigned To (User lookup), SLA Breach Risk (Checkbox), and Resolution Time (hrs).
* **Automation**: Auto-Launched Flow (`Support_Ticket_Intellegence`) configured to handle backend data routing and updates.
* **AI & Agentforce**: Subagent (`Support Ticket Priority Analysis`) integrated with Agentforce actions to evaluate issue urgency, categorize support requests, and fetch record-by-record structured output (including Ticket Number, Created Date, and Owner ID).

## 📋 Features
* **Automated Priority Assessment**: Automatically evaluates customer support tickets based on issue description and urgency.
* **Conversational Insights**: Allows support staff to interact with Agentforce using natural language prompts (e.g., *"give me my support ticket data"* or queries filtered by Account Name) to instantly retrieve ticket summaries and details.
* **Structured Record Outputs**: Displays comprehensive ticket attributes cleanly within the conversation preview interface.

## ⚙️ Setup & Configuration Steps
1. **Salesforce Custom Object Creation**:
   * Created the `Support Ticket Intelligence` object with proper API naming conventions.
   * Configured relationships including Account and Contact lookups.
2. **Field Definitions & Layouts**:
   * Added custom picklists for `Issue Type` (`Technical`, `Billing`, `General`) and `Priority Level`.
   * Set up tracking fields like `SLA Breach Risk` and `Resolution Time`.
3. **Agentforce & Subagent Integration**:
   * Linked the custom object actions to the `Support Ticket Priority Analysis` subagent.
   * Refined agent instruction prompts and output mappings to ensure accurate record-level reporting.

## 🚀 How to Use
1. Navigate to the **Agentforce Builder** or your custom Salesforce App.
2. Enter prompts such as querying tickets by Account Name (e.g., `ABCD`) or requesting a full list of support ticket statuses.
3. Review the real-time conversational preview output detailing ticket numbers, creation dates, and owners.

## 📄 Documentation
Additional project artifacts, screenshots, and structural schemas can be found within the repository files.
