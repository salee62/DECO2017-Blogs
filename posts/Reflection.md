---
title: DECO2017 Reflection
date: 2026-06-09
author: Winnie Eap
summary: Assignment Reflection
tags:
  - reflection
  - usability
  - evaluation
---
## Introduction
Looking back on the project, one of the most significant design decisions involved determining which feature should become the platform's primary interaction. While the project was always intended to include a distinctive feature that differentiated it from existing community platforms, early concepts explored several possibilities including forums, court discovery, profiles, and events. Through design iteration, development, and evaluation, the event system became the strongest opportunity to support the needs of badminton players. As a result, the platform evolved towards an event-centred experience with supporting features designed to complement participation rather than compete with it.

## Performance
The application demonstrated strong loading performance across both desktop and mobile devices in Lighthouse testing. The lightweight stack of HTMX, SQLite and lack of heavy frontend frameworks, reduced unnecessary overhead, resulting in fast rendering times and minimal blocking during page load. 

Lighthouse testing on a Macbook indicates that the prototype performed strongly, achieving a score of 100 on desktop and 92 on mobile. For the homepage, the desktop report recorded a First Contentful Paint (FCP) of 0.6 seconds and Largest Contentful Paint (LCP) of 0.7 seconds, while mobile performance was lower with a 1.8 seconds FCP and 3.2s LCP. Unlike heavier frontend frameworks, HTMX allowed interface updates such as RSVP interactions and filtering to occur without loading large JavaScript bundles, contributing to the application’s low blocking times. These results suggest that the homepage performed efficiently overall but mobile users were more affected by image loading and render-blocking resources. 

<img src="assets/images/lighthouse-desktop.png" alt="Lighthouse" width="90%">

**Figure 1. Lighthouse Desktop Homepage Score**

<img src="assets/images/lighthouse-mobile.png" alt="Lighthouse" width="90%">

**Figure 2. Lighthouse Mobile Homepage Score**

<img src="assets/images/lighthouse-events.png" alt="Lighthouse" width="90%">

**Figure 3. Lighthouse Desktop Event Page Score**

While the homepage achieved excellent Lighthouse scores, testing was also conducted on the events listing page, which represents the primary user workflow of the platform. On desktop, the events page maintained a FCP of 0.6 seconds and a LCP of 2.4 seconds indicating that users could begin interacting with content quickly despite the additional event images and card based layouts. However, mobile testing revealed a large performance gap with a FCP of 1.8 seconds and a LCP of 13.7 seconds. While users received initial visual feedback relatively quickly, the main event content took significantly longer to fully load on mobile devices. This would indicate that image heavy content and card based layouts introduced additional overhead, highlighting an area for future optimisation. Overall, the performance for the events page for desktop was 87 and mobile 74.

The Best Practices score of 70 highlighted several technical limitations that would need to be addressed before being properly deployed. Lighthouse identified issues such as missing HTTPS configuration, browser console errors, unminified assets, and unused CSS and JavaScript. While these issues did not significantly affect the functionality of the prototype, they indicate opportunities for further optimisation and improved maintainability.

These findings align with my expectations for the project. Testing focused particularly on the events page because event discovery and participation represented the platform’s primary user workflow. While desktop performance remained strong, mobile testing revealed opportunities for improvement that were not immediately apparent from homepage testing alone. Development efforts were prioritised towards implementing core functionality such as forums, a map of courts, and event creation and RSVP. Given more time, further improvements would focus on improving mobile optimisation, asset delivery and deployment considerations to improve performance across a wider range of devices and network conditions. 

## User Experience

<img src="assets/images/thinkaloud-summary.png" alt="Think Aloud" width="90%">

**Figure 4. Summary of Think Aloud findings**

Think Aloud testing with five participants suggested that event discovery was one of the strongest aspects of the platform. All participants successfully located the Events page and were able to identify suitable sessions without assistance. Four participants specifically mentioned the usefulness of the skill-level filtering system, suggesting that it reduced the effort required to browse large numbers of events. Event cards provided users with key information such as skill level, location and participation details without requiring unnecessary navigation. This reduced the number of interactions required to evaluate potential sessions and helped users make decisions more efficiently.  As shown in Figure 4, all participants were able to complete the event discovery task successfully, while four participants specifically commented on the usefulness of the filtering system when narrowing down suitable sessions.

<img src="assets/images/event-card.png" alt="Event Card" width="50%">

**Figure 5. Event Card**

During development, profiles were not prioritised within the scope with a bigger focus on the forums, maps, and events. Our earlier concepts attempted to balance other features equally as well as including messaging and interaction, however, this risked creating a more complex navigation structure. Narrowing the platform’s focus towards event participation reduced navigational complexity and created a clearer information hierarchy centered around event participation. In retrospect, this decision improved usability by aligning the platform more closely with the needs of badminton players seeking opportunities to play.

All five participants were also able to complete the RSVP task without assistance and immediately recognised when their booking had been confirmed, suggesting that the event workflow was intuitive and easy to understand. However, testing revealed limitations in the mobile experience. The responsiveness for mobile device layouts were not fully optimised, especially given different screen sizes, which occasionally reduced readability and required additional scrolling compared to the desktop experience.

Lighthouse Accessibility testing produced a score of 92, indicating a strong foundation. Semantic page structure and image alternative text contributed positively to accessibility, while testing identified several areas for improvement, particularly colour contrast and form labelling. Additional manual testing was conducted using keyboard navigation, with tab ordering remaining logical across key interactions such as event browsing and filtering. Although these results suggest that accessibility was considered during development, further improvements to achieve a greater WCAG AA compliance would require more consistent form labelling, improved colour contrasted, and further testing with assistive technologies.

## Functional Requirements
Looking back at the functional requirements identified during the planning phase, most were successfully implemented within the final prototype, although some evolved considerably throughout development.

Content sharing was originally identified as a core requirement and was implemented through both forum discussions and event creation. However, during development it became clear that placing too much emphasis on traditional social content risked making the platform feel similar to existing social media applications. As a result, event creation and participation became the primary focus ultimately becoming the main way users interacted with the platform.

Content interaction was achieved through RSVP functionality, event participation visibility, and forum discussions. While the forum supported community discussion, testing and development suggested that users gained more value from interacting through events than through traditional discussion based content. 

Usability was also identified as a key requirement during early planning. Features such as skill filtering, event cards, consistent navigation and predictable interaction patterns helped support this goal. Testing suggested that users could quickly identify relevant sessions and complete common tasks without excessive navigation. However, mobile responsiveness limitations demonstrate that this requirement was not fully achieved across all devices.

While the brief always required a distinctive feature, early concepts explored several possibilities including forums, maps, profiles, and events. Through iteration and testing, the event system became the platform's strongest differentiator and became the primary focus of the final prototype. In hindsight, prioritising this feature earlier may have improved development efficiency and reduced time spent exploring less impactful alternatives.

## Lessons Learned
The project improved my understanding of how design decisions and technical decisions influence one another. During the planning phase, many ideas appeared feasible from a design perspective but implementation introduced additional constraints related to database structure, routing, responsiveness, and performance. This highlighted the importance of considering technical feasibility alongside user needs rather than treating them as separate concerns.

Another important lesson involved accessibility and evaluation. Prior to testing, I assumed that a visually clear interface would naturally be accessible. However, Lighthouse audits and accessibility checks revealed issues such as colour contrast and form labelling that were not immediately obvious during development. This demonstrated the importance of incorporating accessibility evaluation throughout the design process rather than treating it as a final validation step.

Finally, the project reinforced the importance of iterative development. Many of the strongest design decisions, including prioritising the event system and simplifying navigation, emerged through repeated refinement rather than during the initial planning stages. This experience showed that successful web applications are not created through a single design decision but through continuous evaluation, testing, and adaptation as requirements become clearer.
