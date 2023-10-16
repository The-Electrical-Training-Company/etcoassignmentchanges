## Etco changes to the Moodle core Assignment Plugin
\
Changes have been made to the core Moodle assign code to limit the permissions of some roles, add new permissions, and rework the marking workflow to better align with Etco's process.

---

&nbsp;
## Modifications
* Add setting to disable 'quickgrading'.
* Only 'Assessors' appear in 'Allocated marker' drop down.
* Allow 'Allocated marker' to be assigned at the same time as workflow moved to 'readyforreview' from 'Grade' page.
* Add requirement for user to have mod/assign:completemarking capability to see marking allocated to them, users without this capability but with the mod/assign:grade capability can see users in their group without the need to have them assigned.
* Restrict users without the mod/assign:completemarking capability to only access the first two steps of the marking workflow.
* Only 'Assessors' can edit the grade value.
* Add notification to marker when allocated to submission.
* Add notification to student when submission reverted to draft.
* Update notification links to take user directly to submission rather than overview page (if recipient has mod/assign:viewgrades).
### Latest - October 2023
---
* Create simplified version of mod_assign_get_submissions(_basic) with only fields required for automatic marker allocation.
* Modify mod_assign_set_user_flags to log an event when a marker is allocated via API.
* Create mod_assign_get_available_markers to list markers able to assess assignments.

&nbsp;
## New capapbilities
* Complete marking workflow step (mod/assign:completemarking) - restricts users who can complete the marking workflow step (restrict workflow state options).
* Appear in Marker list (mod/assign:assessor) - only users with this capability appear in the 'Allocated marker' drop down list.
* View markers allocated to submissions (mod/assign:viewallocations) - users with this capability can view the allocated marker but cannot edit.

&nbsp;

---
These changes were made by Andrew Chandler (andrewc@etco.co.nz) for The Electrical Training Company Ltd. (Etco) and are not intended to be used outside of Etco's environment.

