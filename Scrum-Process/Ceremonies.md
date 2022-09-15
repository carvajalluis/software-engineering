# Ceremonies
[[_TOC_]]
# Sprint Refinement 
 To ensure that each story marked as "Ready for Development" is understood by the entire development team and risk of development is minimized. To minimize risk, a story must have all of its details regarded it's business value and its user experience and, have any technical questions/comments/notes that need further clarification in the stories development research task be documented by the Developer Note Taker and provide research direction for the assigned developer once the this story is included in a sprint. All stories coming out of the refinement meeting as "Ready for Development" must have story points assigned.
## Roles
  - Scrum Master (Required):
    - Our grooming sessions are managed by the SCRUM Master who is responsible for keeping the pace of the meeting. They are responsible for ensuring:
    - No stories that should remain in discovery are marked as ready for development
    - No question are left unasked
    - Only stories with all required fields are part of the grooming session
    - The assigned developer is indeed taking notes
    - All members are participating in the discussion
    - All required fields are satisfied before moving stories to Ready for Development
    - Record and organize the recording for the meeting and ensure it is accessible to development team.
  - Product Owner (Required):
    - The product owner is responsible for describing the business value of the story, the acceptance criteria for the story, walk through any relevant mockups, and communicating all absolute requirements. If any questions arise that require the story to be reevaluated or further defined, the Product Owner will be taking notes in an external software which will later be used to further develop the story.
  - Developer Note Taker (Required):
    - A member of our development team will be assigned to take Development Notes during the grooming session. This role will be assigned by the SCRUM Master at the beginning of the meeting. This role is responsible for ensuring that all technical questions/notes/comments are recorded within the Developer Notes section of the story. **They are the only ones able to edit the story during these sessions.**
## Rules
  -  If any questions or unknowns are brought up during grooming sessions, the story is not moved forward to "Ready for Development"
 - No additional acceptance criteria can be recorded during these sessions. 
  - Only the Developer Note Taker may edit the story during these sessions.
  - Refinement meetings will be recorded and available here: 

[back to the top](#ceremonies)

---
# Sprint Planning
The sprint planning meeting is held by the SCRUM Master and Product Owner. The goal of this meeting is to inform the development team of the goals of the upcoming sprint and ensure that the stories included have all dependencies satisfied. This is the 'semi-final' point any members of the development team can bring up any issues with stories and the final point where the Product Owner can modify stories included in the upcoming Sprint.

## Roles
- SCRUM Master (Required):
  - Assist as a communication liaison
  - Ensure meeting is staying on track 
  - Scheduling Meeting
  - Ensure that dev team capacity is properly identified and mapped for the Sprint. This includes identification and logging of any time off.
  - Review Sprint Timeline
- Product Owner (Required):
  - Ensure that all stories to be included in sprint are finalized before the meeting
  - Walk through the stories and provide a brief description as to their business value and what the user experience should be
  - Answer any remaining questions from the developers
- Architect/ Development Lead (Required):
  - Identify any architectural questions remaining and, if answers are not able to be provided prior to Sprint, request the removal of such items.
  - Ensure firm understanding of each story in Sprint
- Development Team (Required):
  - Ensure a firm understanding of each story in the Sprint
  - Identify and voice any concerns with items in the sprint
  - Ask Questions to ensure complete understanding of the tickets in the Sprint
  - Remind SCRUM Master of any time off during the sprint or any items that might affect their capacity.

## Rules
  - The SCRUM Master will provide an overview of the planned Sprint by reviewing the Sprint calendar including important dates, number of days off for any of the development team, outline any meetings during the sprint, and ensure that everyone is aware of the final Story Points to be included in the Sprint.
  - Once the Sprint overview is completed, the Product Owner will briefly describe each item in the sprint and review it's business value.
  - Any team member may ask clarifying questions at any point during this ceremony.


[back to the top](#ceremonies)

---
# Sprint Launch
The sprint launch meeting is held by the Systems Architect. The goal of this meeting is to finalize the Sprint by reviewing tickets that carried over from the last sprint (if any) and assigning all tickets to developers to evenly distribute the workload and maximize the effective use of everyone skill sets. 
## Roles
- Architect/ Development Lead (Required):
  - Briefly review each ticket and assign it to the team member best fit to successfully complete.
  - Assign work items to best fit developer
- Development Team (Required):
  - Ensure that any concerns over their own individual capacity or capability of completing a given item is heard, understood and accounted for by the Architect/Development Lead as they are assigned stories. 
- SCRUM Master (Optional):
  - Assist as a communication liaison. 
## Rules
  - If at this point the Sprint is deemed over capacity, items can be requested for removal by the development team. To remove an item, it must be requested to the SCRUM Master, verified with the Product Owner, and then can be removed from the Sprint by the SCRUM Master.

[back to the top](#ceremonies)

---
# Daily SCRUM

The goal of the Daily SCRUM is for each developer to update the Development Team on their progress and to identify any blockers associated with their work items. It is also an opportunity for any developer to request assistance for any issues they're having a hard time tackling with their story or any novel risks associated with their work items. 
## Roles
 - SCRUM Master:
   - Enforce pace of meeting and meeting rules
   - Request statuses of each of the developers
   - Ensure that stories are updated with work completed (in story points) and work remaining (in story points)
   - Identify any potential capacity issues or risk-of-carryovers and communicate these to the Product Owner
- Development Team:
  - Providing an update to their status on each story including:
    - Any blockers
    - What their working on now
    - Any risks they see in completing their assigned stories for the Sprint
  - Identify any items they'd like assistance on or for the Architect/Development Lead to review for Architectural accuracy and Functional Optimization
- Architect/Lead Developer
  - Ensure that the status described by each developer is in line with Architectural and Development Standards for the system. 
  - Proactively request that the developer reviews any database modifications or complex functions with them in a separate meeting.
- Product Owner (Optional)

## Rules
  - Only limited detailed technical discussions should take place during the Daily SCRUM. Any technical questions requiring more than 2 minutes to answer or discuss should be identified and held to discuss at the end of the meeting where only relevant parties will stay on to continue discussion or, if there are a large number of items or the discussion is expected to take longer, a separate time should be set up to review. **The SCRUM Master is responsible for enforcing this rule and aiding in scheduling.**
  - The SCRUM Master will choose the order in which each developer is to present their status.

[back to the top](#ceremonies)

---
# Sprint Demo
The Sprint Demo is to be run by the Systems Architect/Development Lead. The Sprint demo is to showcase the teams work during the Sprint to the Product Owner. For items that have a complete loop in terms of front-end and back-end, those items will be showcased via a front-end demonstration with database showcasing as necessary. For items that are only represented by backend code, these items will be showcased by flowcharts, diagrams, and live API requests/responses that should be created during the research phase of the story.

## Roles
- Architect/ Development Lead (Required):
  - Briefly review each ticket, explain its functionality and pass to QA Engineer for demonstration
  - Work with QA Engineer to create demo
- QA Engineer (Required):
  - Demonstrate ticket if it is a 'complete loop'. If it is only a backend item, the architect/development lead will request that the developer who was assigned to this story showcase their work.
- Development Team (Required):
  - Come prepared with all tools and documentation necessary to showcase each of their assigned and completed items.
- SCRUM Master (Required):
  - Assist as a communication liaison. 
- Product Owner (Required):
  - Verify that the functionality or outcome of each item in the completed Sprint is acceptable.

## Rules
  - After each demonstrated story, the SCRUM Master will request verification from the Product Owner that the item was completed and fits the desired outcome. As each story is verified, the SCRUM Master will mark the story as Passed Demonstration indicating that it is indeed, ready for release


[back to the top](#ceremonies)

---
# Sprint Retrospective
The purpose of the Sprint Retrospective is to plan ways to increase quality and effectiveness.

## Roles
- The Scrum Team  (Required):
  - The team will inspects how the last Sprint went with regards to individuals, interactions, processes, tools, and their Definition of Done.
  - The Scrum Team will discusses what went well during the Sprint, what problems it encountered, and how those problems were (or were not) solved.
  - The Scrum Team identifies the most helpful changes to improve its effectiveness. 
  - The most impactful improvements are addressed as soon as possible. They may even be added to the Sprint Backlog for the next Sprint.
- SCRUM Master (Required):
  - Assist as a communication liaison.

## Rules
- The Sprint Retrospective concludes the Sprint. It is timeboxed to a maximum of 30 mins for a two-week Sprint.

---
# Sprint Cadence
