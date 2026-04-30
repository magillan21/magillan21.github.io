---
layout: essay
type: essay
title: "Pretty In Patterns: A Romantic Comedy"
# All dates must be YYYY-MM-DD format!
date: 2025-04-29
published: true
labels:
  - Design Patterns
  - Study-Viser
  - Software Engineering
  - Web Development
---

## 50 First Construction Dates or How to Build a City in 10 Days?
 
Imagine two cities. The first city was built reactively: a road was built there because a farmer needed to reach a market, a building was built there because land was cheap, a bridge was thrown up because there was a flood. The city works! …Technically. People *can* get from place to place. But nobody can explain why the farm is right in front of the bakery, or why the post office is stuck between two parking garages with basically no entrance. Everyone who moves there has to figure things out. 
 
The second city was designed by people who had built cities before. They knew that residential areas should buffer industrial zones, that town centers create gathering points, and that a grid system allows some semblance of organization. They didn't invent these concepts or ideas, but they were able to learn from architects before them and adapt it to a new terrain. 
 
Software faces the same issues, I think. Code written without shared vocab becomes the first city: the author knows what’s going on… but does everyone else? Design patterns are the architectural vocabulary that help create the second kind of codebase/city. Organized and extendable.
 
---
 
## How I Met Your Pattern

In my final project, StudyViser, a collaborative academic platform where instructors define glossary terms, students compete to submit the best definitions, and the highest-quality entries are approved for a compiled, interactive course resource.
The most visible pattern in StudyViser is the Strategy pattern. The app has three user roles: Student, Instructor, and Teaching Assistant, and each one behaves differently. Instead of writing a bunch of if user.role == "instructor" checks all over the place, each role's behavior gets packaged into its own strategy. The app just picks the right one based on who's logged in, which also makes it easier to add a new role down the line without touching existing code.

The submission cap logic (where courses with 1–20 students allow 3 submissions per term, 21–40 allow 4, and 41+ allow 5) is another home for the Strategy pattern. The cap-calculation algorithm is interchangeable and selected at course-creation time based on enrollment size, so the submission service never needs a chain of if/else branches to determine the current rule; it simply delegates to whichever strategy is in effect.

The Observer pattern looks over the credit and glossary pipeline. A glossary term's approval status is the subject; the extra-credit ledger and the course glossary index are observers. When a TA approves a submission, that single state changes fans out automatically: the selected student's extra-credit balance is updated, and the approved definition is published to the official glossary. The remaining submissions are simultaneously re-tagged as supplementary resources.

---

## Clueless…

<img width="500px" class="rounded float-start pe-4" src="../img/maxresdefault.jpg">

Once you learn design patterns, it's tempting to use them everywhere… But patterns exist to solve specific problems, and using them where there isn't one just makes the code harder to follow, even if you feel more clever or comfortable. 

The more useful thing patterns give you is a shared vocabulary. When someone opens a file and immediately recognizes an Observer or a Facade, they don't have to reverse-engineer what it's doing. That speeds up code reviews and feels a lot less like pulling teeth for the next person to pick up where you left off. Just be cautious, choose a pattern that’s in-fashion for your goals.

Which is kind of the whole point. Like a good city, good software should be something other people can navigate too.



