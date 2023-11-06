#  Custom UC: Health Community Forum

## User Stories
### Case 1: User Views Forum Discussions
A patient logs into the iTrust platform and accesses the Health Community Forum. They are looking for information related to diabetes management. They enter the keyword 'diabetes' into the search bar and then receive a list of discussions about diabetes containing valuable insights shared by other users.

### Case 2: Patient Creates a Discussion Thread
A patient seeks guidance regarding unusual symptoms they are experiencing and wants to identify the appropriate clinic department to book an appointment based on their symptoms. They  create a new discussion thread, explaining their symptoms briefly. After a while, they receive a reply from a healthcare professional recommending that they book an appointment with Doctor X in the Y department.

### Case 3: HCP Creates a New Discussion Thread
A HCP who is a nutrition specialist,  accesses the Health Community Forum and creates a new thread titled "Healthy Eating Habits for Busy Professionals," initiating a conversation about balancing nutrition for individuals with busy schedules.

## Preconditions 
An authenticated user, either a patient or a healthcare provider (HCP), is registered and logged into the iTrust platform.

## Main Flow
The authenticated user accesses the Health Community Forum from the platform's main dashboard. They can view and participate in various health-related discussions, create new discussion topics, reply to existing threads, and engage in conversations with other users.

## Sub-flows
Users can search for specific health topics using a search bar to find related discussions. Users can create new discussion threads, including asking questions, sharing personal experiences, or providing insights on different health-related matters.
Users can reply to existing discussion threads, offering advice, sharing links to resources, or engaging in meaningful conversations.

## Alternative Flows
If a user's search query does not match any existing discussions, a message indicating no results will be displayed.
In case of inappropriate content, users can report or flag the discussion for platform moderators (a.k.a admins and HCPs) to review and take necessary actions.

HCPs have the authority to erase any of the entries or replies created by patients. If a HCP replies to a thread, their response is displayed prominently at the top of the thread, labeled with a verified badge, indicating that the information provided is verified.

## Logging
|Transaction Code | Verbose Description | Logged In MID | Secondary MID | Transaction Type | Patient Viewable|
|-----------------|---------------------|---------------|---------------|------------------|-----------------|
2301             | User views forum discussions        | patient |    -    | View   | Yes
2302             | User creates a new discussion thread| patient |    -    | Create | Yes
2303             | HCP creates a new discussion thread | HCP     |    -    | Create | Yes
2304             | User replies to a discussion thread | patient | patient | Create | Yes
2305             | HCP erases a patient entry/reply    | HCP     | patient | Delete | No
2306             | User reports a certain entry/reply  | patient | patient | Create | Yes
2307             | HCP replies to a discussion thread  | HCP     | patient | Create | Yes


## Data Format
|       Field       |        Format       |
|-------------------|---------------------|
Discussion Topic    | Text, up to 100 characters
Discussion Body	Text| Text, supports up to 1000 characters
Discussion Reply    | Text, supports up to 1000 characters


## Acceptance Scenarios
Scenario 1: User Views Forum Discussions
Patient Adam logs into the iTrust platform and accesses the Health Community Forum. He searches for discussions related to diabetes management and finds valuable insights shared by other users.

Scenario 2: Patient Creates a Discussion Thread
Patient Jane logs into the iTrust platform and navigates to the Health Community Forum, she seeks guidance regarding unusual symptoms she's experiencing. Jane wishes to identify the appropriate clinic department to book an appointment based on these specific symptoms.

Scenario 3: HCP Creates a New Discussion Thread
HCP Dr. David, who is a nutrition specialist,  accesses the Health Community Forum and creates a new thread titled "Healthy Eating Habits for Busy Professionals," initiating a conversation about balancing nutrition for individuals with busy schedules.
