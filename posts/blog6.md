---
title: Evaluating and Revisiting Design Decisions
date: 2026-05-18
author: Winnie Eap
summary: This post reflects on the final platform direction and discusses future improvements and testing considerations.
tags:
  - reflection
  - usability
  - evaluation
---
### Reflection
At the beginning of the project, the main challenge was interpreting what BlaBla Corp meant by a “community hub” and identifying what would make the platform feel different from existing social media platforms.

Initially, we focused the project on exploring multiple directions including forums, maps, events, and profiles. However, throughout the design process it became clear that simply combining common social features would not create a strong enough identity for the platform. As the project developed, the event system gradually became the platform’s standout feature. This decision aligned more closely with the needs of badminton players who are primarily looking for opportunities to participate in games, connect with players of similar skill levels and engage with the community through real world interactions.

Looking back, narrowing the focus towards event interaction did significantly improved the overall clarity and direction of the platform as said in my first blog post.

### Usability & Evaluation
Visual hierarchy, readable typography, colour contrast, and consistent interaction patterns were used to improve clarity and navigation across the platform for usability. The design system also helped maintain consistency between pages by standardising typography, buttons, and interface components.

Although the platform has been designed with accessibility in mind, there are still several areas that would require further evaluation if the project continued. In order to do so, one of the main goals we had throughout the project was identifying which features were essential and which features could function as supporting systems.

The final platform prioritised:
- Event discovery  
- Skill-based filtering  
- RSVP interactions  
- Event participation visibility  

These features were prioritised because they directly support the platform’s main purpose of helping badminton players discover and join suitable sessions. Other systems such as forums, maps, and profiles still remain important, but they became secondary features that support the main event interaction flow rather than competing with it. This helped reduce unnecessary complexity and kept the platform more focused. Earlier stages of the project introduced many possible features, but revisiting the brief and reassessing user needs helped refine the overall scope.


Whilst developing, technical decisions became closely connected to functional requirements and feasibility. Since the platform needed to support lightweight interactions within the required stack, technologies such as HTMX and SQLite became practical choices we had to use for the project. HTMX supported smaller interface updates such as filtering and RSVP interactions without requiring more complicated frontend frameworks. SQLite also suited the project scope by providing a lightweight way to manage event and forum data. At the same time, the project involved several compromises. Some features originally considered during early ideation stages were simplified or reduced in scope to ensure that the event system could be developed more effectively. This reinforced the importance of prioritising depth over breadth. Rather than attempting to fully develop every feature equally, focusing on the platform’s core interaction created a more cohesive and realistic prototype.

### Future testing
- Accessibility testing against WCAG AA standards  
- Mobile responsiveness testing  
- User testing for RSVP and filtering interactions  
- Performance testing for event loading and search systems  

These evaluations would help identify usability issues and ensure that the platform performs effectively across different devices and user contexts.

### Final Reflection
This project demonstrated how design ideas can evolve significantly throughout development. Earlier ideas we had focused on creating a broad badminton community platform, but over time the project became more focused on refining a smaller number of meaningful interactions. The process also highlighted the importance of balancing ambition, usability, and technical feasibility. Revisiting earlier assumptions and refining priorities helped create a clearer and more realistic platform direction.

Overall, the project reinforced that strong community platforms are not defined by the number of features they contain, but by how effectively their core interactions support the needs of their users.