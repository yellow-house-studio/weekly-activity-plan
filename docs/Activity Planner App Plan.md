# Activity Planner App Specification

## Overview
A web application designed to help schedule and suggest activities for a family based on participants' availability, preferences, and contextual factors like weather and recurring patterns. The app integrates with Google Calendar and provides a robust system for planning and reviewing activities.

---

## Features

### 1. Weekly Planner View
#### Purpose:
- Plan and schedule activities for the week (Monday–Sunday).

#### Components:
1. **Weekly Grid**:
   - Displays days (Monday–Sunday) with configurable time slots (default: 7 AM–7 PM).
   - Time slots are divided based on user-defined granularity (e.g., hours, morning/afternoon/evening).
   - Pre-populates with:
     - Existing calendar events (greyed out, not editable).
     - AI-suggested activities (color-coded).
     - Free slots for planning.

2. **Activity Pool (Sidebar)**:
   - Contains replaced suggestions, recurring activities, and AI-generated alternatives.
   - Drag-and-drop enabled for assigning activities to slots in the weekly grid.
   - Searchable and filterable by tags, type, or participant suitability.

3. **Slot Controls**:
   - **Accept Suggestion**: Confirm the suggested activity.
   - **Replace Activity**: Swap with an alternative or manual input.
   - **Mark as No Activity**: Indicate no activity for the slot.

4. **Participants**:
   - Visual indicators for availability.
   - Alerts for conflicts (e.g., parent or child unavailable).

5. **Feedback Options**:
   - Icons for marking activities as:
     - "Great Choice" (starred).
     - "Did Not Work Out" (optional comments).
     - "Not Done" (skipped).

#### Workflow:
1. Open the planner.
2. Review and adjust AI-suggested activities.
3. Replace, accept, or manually add activities as needed.
4. Save the plan and sync with Google Calendar.

---

### 2. Week Summary View
#### Purpose:
- Review the past week to refine future suggestions.

#### Components:
1. **Completed Activities**:
   - List of all activities with details:
     - Time slot.
     - Participants.
     - Status (completed, skipped, failed).

2. **Feedback Section**:
   - Buttons for:
     - "Great Choice" (starred).
     - "Did Not Work Out" (optional comment).
     - "Not Done" (missed with optional tags).
   - Quick tags for feedback (e.g., "too long," "kids enjoyed").

3. **Recurring Activities**:
   - Highlight recurring activities and whether they were completed.

4. **Missed Activities**:
   - Show missed activities and allow tagging as "not wanted."

5. **Suggestions for Next Week**:
   - AI-generated insights (e.g., "Outdoor play worked well in the afternoon; consider more activities at this time").

#### Workflow:
1. Review completed and missed activities.
2. Provide feedback and notes for improvement.
3. Save feedback to refine future suggestions.

---

### 3. Activity List View
#### Purpose:
- Manage a central repository of activities.

#### Components:
1. **Activity Table**:
   - Columns for:
     - Name.
     - Type (indoor/outdoor).
     - Tags (e.g., creative, active).
     - Duration.
     - Weather dependency.
     - Recurrence status.
   - Sort and filter by type, tags, age suitability, or popularity.

2. **Manual Input**:
   - Add new activities with attributes like name, type, duration, and tags.
   - Edit existing activities.
   - Delete unused activities.

3. **Integration with Planner**:
   - Drag-and-drop functionality to assign activities to the planner.
   - Highlight popular or frequently used activities for quick selection.

#### Workflow:
1. Browse the activity list.
2. Add, edit, or delete activities as needed.
3. Use filters to find relevant activities for manual planning.

---

### 4. Settings View
#### Purpose:
- Customize app behavior and preferences.

#### Components:
1. **General Settings**:
   - Timespan for Scheduling: Configurable start and end times (default: 7 AM–7 PM).
   - Default Duration: Set the default length for activities.
   - Notification Preferences: Enable/disable reminders.

2. **Participant Settings**:
   - Assign calendars to participants.
   - Define inclusion rules:
     - "Always" (always included).
     - "When name/nickname is included" (conditionally included).
   - Set school schedules and busy times.

3. **Recurring Activities**:
   - View and manage marked recurring activities.
   - Adjust recurrence settings (e.g., flexible vs. fixed).

4. **Weather Preferences**:
   - Configure thresholds for weather-dependent suggestions.

5. **Database Management**:
   - Export/import activity data.
   - Clear historical feedback.

6. **AI Tuning**:
   - Adjust how feedback influences future suggestions.
   - Enable/disable specific suggestion sources.

#### Workflow:
1. Navigate to settings.
2. Adjust preferences as needed.
3. Save changes to apply immediately.

---

### Additional Requirements
1. **Parent Availability**:
   - Activities can only be scheduled if the parent is free.

2. **Timespan Constraint**:
   - Activities can only be scheduled within a configurable time range (default: 7 AM–7 PM).

3. **Database**:
   - Maintain a central repository of activities and associated metadata to:
     - Provide context for AI suggestions.
     - Support manual inputs that don’t fit into the calendar.

---

## Next Steps
- Finalize database schema to support planner and activity views.
- Design backend APIs for:
  - Calendar integration.
  - Activity suggestion engine.
  - Participant availability rules.
- Build frontend components for the planner and settings views.

---
