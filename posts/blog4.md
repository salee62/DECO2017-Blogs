---
title: Prioritising Features and Planning Development
date: 2026-05-12
author: Winnie Eap
summary: This post explores how the group prioritised features, organised development tasks, and focused on building the community platform.
tags:
  - project planning
  - feature prioritisation
  - technical decisions
---
### Project Planning
After refining the wireframes and interaction design, the next step was planning how the platform would actually be developed. Since the project includes multiple systems such as events, forums, maps, and profiles, it became important to organise tasks clearly and decide which features needed the most focus. To manage this, the group created a Kanban board to organise development tasks and track progress throughout the project.

<img src="assets/images/kanban.png" alt="Kanban Board" width="90%">

**Figure 1. Kanban Board to organise tasks**

The Kanban board helped divide tasks into categories such as “to-do”, “in progress”, and “done”. This made it easier to visualise what still needed to be completed and helped the group stay focused during development.

The board also helped split responsibilities across the team. My tasks mainly focused on the events system, including:
- Creating the events page and event listing system  
- Developing RSVP interactions  
- Building the create event form  
- Implementing event search and skill filtering  
- Structuring the SQL schema for event data  
- Creating routes for event-related pages  

This helped maintain a clearer development direction while ensuring that the platform’s main interaction system continued progressing.

### Feature Prioritisation

Although the platform contains several features, the events system became the main development priority. Earlier wireframe exploration showed that event based interaction created the strongest opportunities for engagement, especially since badminton communities revolve around real world participation. Because of this, more development time was spent refining event interactions rather than expanding secondary systems. This included:
- Skill-based filtering  
- RSVP interactions  
- Event discovery  
- Event participation visibility  

Focusing on these areas helped strengthen the platform’s standout feature and made the event experience feel more tailored to badminton players instead of functioning as a generic event listing system.

### Technical Decisions

As development planning continued, the group also needed to consider how these interactions would function technically within the required stack. One important consideration was how to keep the platform lightweight while still supporting responsive interactions. Features such as filtering events, RSVP updates, and event creation required both frontend and backend planning. HTMX was useful during this stage as it allowed smaller interface updates without needing complicated frontend frameworks. This made interactions feel smoother while still remaining relatively simple to implement. SQLite was also used to structure and manage platform data such as events, users, and forum content. Since the project focuses on community interaction rather than large scale data processing, SQLite was a practical solution that suited the scope of the prototype.

This stage of the project highlighted the importance of planning and prioritisation throughout development. Organising tasks through the Kanban board helped the group manage scope more effectively and maintain focus on the platform’s core interactions. It also showed that technical decisions are closely connected to design decisions. By focusing on a smaller number of refined interactions, the platform became more realistic to develop while still supporting a meaningful and engaging community experience.

