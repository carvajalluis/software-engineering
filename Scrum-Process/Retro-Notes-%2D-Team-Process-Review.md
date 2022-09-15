Immediate Processes
- Update Points Remaining and Points Completed before each Daily SCRUM
- Technical Solution created and defined before meaningful development starts
- Developers to pick a 1 point ticket to spend some time on each day for the sprint

Soft Processes
- Ensure code reviews cover
  -  Quality of code at hand
  - Dependencies on past code or current tickets

Backlogged:
- Proper Dev Environment
- ZaHub QA Env
 
------------------------------------

# <u>Retro 46<U> 

* START meeting "release plan" 15 min after Kick off 
  * recognize risks 
  * how to mitigate them
* START refactoring guru course share 
  * course synopsis  in wiki
* STOP Adding scope to the stories at half sprint
  * learn story telling  wiki 
  * story splitting wiki
  * acceptance criteria verification during grooming: why, when, how  ? 
  * on new scope discovery validate it what's  expected or not ( triage )
* CONTINUE improving  as engineers
  * wiki proposals during kickoff 
  * share  new training resources for AWS 
* CONTINUE better acceptance criteria
  * clarify what is a well written acceptance criteria 


------------------------------------

# <u>Retro 54

* START 
  * Focusing on Smaller, single responsibility components - adding this as a function of code reviews
  * Each developer on a code review should raise their standards on what passes code review and what doesn't. 
* STOP
   * Giving too much detail within Daily Scrums - Harrison will interrupt moving forward... don't take offense :)
* CONTINUE
   * Adhering to Rest API Design and MongoDB Schema best practices
   * Cleaning up code when possible
------------------------------------

# <u>Retro 58 - 7/18/2022
## START: 
**Topics need further development:**  
* Need Test Cases  available for User Story earlier in Sprint. Possibly before/during refinement.
   * Should this be added as a new State?   
   * Test Cases need to be linked to Story

**Detailed Research on Stories before development**
 * Tech solutions should be defined before development work 
 * If proper research is handled up front, it will help eliminate bugs and developer will have better flow when programming  
* To make sure the research is being properly cared for, we (PO/LA/SM) created new States to care for defining research and getting research approval before programming can begin.  
* Goes in affect Sprint 59 
* Need to confirm protocol on forwarding research to Luis? Where should this live? Make a "Research" tab? Created template and add as an attachment?  
  * Right now, sending wiki link via Teams chat to Luis. Need to organize wiki  


## STOP: 
**Having side effects when adding code changes**
* Double check work 
* Possible solution– hoping the research steps helps eliminate this 

 **QA by Modifying the database by hand** (need to review)
 * In order to test properly need to be able to look at:
    * workflows in the past 
    * Batch jobs in the past
    

## CONTINUE: 
**Keep tight communication when multiple stories touch same codebase:**
* Keep adding common link associations  
* Started group chat to for better communication  
* During Sprint Kickoff speak up if anyone sees similar codebase 
------------------------------------


# <u>Retro 59 - 8/1/2022
 

## START: 
**Adding deployment instructions, needed variables, etc to the research wiki of the ticket**
 * Reorganizing the Research Wiki (Luis) 
 * What is the best archiving system for deployment instructions? Bravo Notes? (Need to review) 

## STOP: 
**Creating bugs without steps to reproduce. Need screenshots of the app and/or videos:**
 * Whoever enters the bug, need to add more details/be specific so the bug can be recreated
 * Assign to Jesus and mark State as "New" 

## CONTINUE: 
**Working in the research documents**
 * Everyone seems to be seeing the benefits thus far 
 * No complaints to date  
 * Teams feels it is not adding more time  
------------------------------------


# <u>Retro 60 - 8/15/2022

## BUG PROTOCOL:

##Keep Doing:         
- Capture bug discovery in full detail. Be specific so the bug can be recreated by including screenshots/videos
- Relate bugs to other bugs/User Stories based on common identifiers  
- Tag appropriately 
- Document trail of bug solution  

##Q: What rules should be made for hot fix bugs?
   
1) Tag as hot fix along with appropriate tags
2) Reorder priority of bug in current Sprint
3) SM to arrange call with PO/LA/Developer
4) SM to alert team of a code freeze on microservice
5) Assigned to Developer and marked as "Active"
6) No need to estimate story points but must finalize Completed and Remaining Story points once Ready for QA

##Q: What is the state process flow for non-hot fix bugs?  
- Assign to QA Engineer and mark as "New", QA Engineer updates to "Discovery" and moves to "Ready for Assignment" 
- If QA Engineer enters bug, he marks as "Ready for Assignment”.
     
*** If developer has completed their workload before end of the Sprint, they can work on any unassigned Bugs (if available)***
*** Any Bugs carried over into next Sprint will be marked as “Ready for Refinement” and given Story Points***

##Q: Are Research steps needed for Bugs?
- Depends on bug 

##Q: How do we make sure unplanned Bug work doesn't affect developer velocity performance?  
- Add "unplanned work" tag

##Q: Should we be capturing reasons for bug carryovering to next Sprint?  
- No. We have an existing field for "Carryover Reason" (same for US), but this is NOT NECESSARY at this time. 

 ------------------------------------

# <u>Retro 61 - 8/29/2022

## START: 
**Suggestion: Grooming items and doing the research before refinement. Keep research process we have now but execute before the item refinement. This will result in better estimate and less uncertainty.**

-What would this look like? 
- Developers would spend time doing research on a ticket for a later Sprint and lose time on the current Sprint
- May limit the developers own thoughts if another developer gets assigned the ticket later
- If we made this change, we would need to explore more of the logistics


## CONTINUE:
With that said, the majority voted that we should continue to do research as we currently are and it's a positive change. 

This idea lead into a conversation if we should be doing a Kanban workflow or possibly a hybrid of Scrum and Kanban. If we did Kanban this would remove story points. As our Sprints look now, we are continuously modifying the workload after the Sprint has started causing us to carry over tickets. Our Sprint goal then becomes unclear and hard to meet. The modification happens because we keep finding bugs. And the purpose of the research is to eliminate the bugs. 

We decided to see how the new Sprint plays out now that Dan is onboard and will circle back on the Kanban suggestion later. 

