# Data flow methodology and diagram

Naan Mudhalvan ID: 88B3FEEAE88BEED87DB4B627DF1EA2E3
Project Title: Optimizing User Group and Role Management with Access Control and Workflows

#### 1. Methodology

The implementation of this project is carried out in several structured steps: Step 1: Creating Users
• Navigate to: All → Users → New
• Create users such as Alice P and Bob P.
• Assign them specific roles and save. Step 2: Creating Groups
• Navigate to: All → Groups → New
• Create groups:
o Project Team
• Submit the groups. Step 3: Creating Roles
• Navigate to: All → Roles → New • Create roles:
o Project Member o Team Member
• Assign each role to its corresponding group. Step 4: Creating a Custom Table
• Go to: System Definition → Tables → New
• Label: Project table & Task Table 2 • Check:
o Create Module o Create Mobile Module Step 5: Assigning Users and Roles
• Assign Alice to the project manager team and give her the following roles:
• Project_Member
• u_project_table
• u_task_table
• Assign Bob to the Team Member team and give him the following roles:
• Team_Member
• Table_role
Step 6: Assigning Table Access to the Applications
• While creating a table, an application and module are automatically created.
• Navigate to: Application Navigator → Search “Project Table” application.
• Click Edit Module → Assign Project_Member role.
• Search Task Table 2 → Click Edit Application.
• Assign Project_Member and Team_Member roles.
Step 7: Setting Access Controls (ACLs)
• Navigate to: System Security → Access Control (ACL) • Create ACLs for the Task Table.
• Add the Team_Member role under Requires Role.
• Create four ACLs for the required fields.
Step 8: Designing the Flow
• Navigate to: Flow Designer → New Flow
• Create a flow “Task Table”
• Trigger: When a record is created in Operations Related
• Condition: Status is: In progress AND comments is feedback AND assigned to is bob
• Action: Update record → Status completed

#### Architecture Diagram

Below is the workflow architecture of the automation system
