---
layout: essay
type: essay
title: "Effort Estimation"
# All dates must be YYYY-MM-DD format!
date: 2026-05-03
published: true
labels:
  - Software Engineering
  - Effort Estimation
  - Group Project
  - Study-Viser
---

<img width="200px" 
     class="rounded float-start pe-4" 
     src="../img/rabbit-watch.png" >

## How was it estimated?
Estimates for StudyViser were made task by task. Each GitHub issue got broken down mentally before any code was written. The idea was that small pieces would add up to something accurate, which did not prove to be fully true.
The thing that threw off almost every estimate was integrating code with previous code. A feature like the TA approval flow looked straightforward until it revealed itself as a transaction problem, an auth problem, and a state sync problem all at once. Anything that touched multiple layers of the stack took longer than it looked. Anything that lived in one place ran pretty close to estimate. There was no historical data to pull from at the start, so early estimates were educated guesses. 

## Did it help?
Yes, although the value wasn't really in the accuracy. Being forced to think through a task before starting it was the most useful takeaway from the experience. Estimating the submission cap logic meant sitting with the rules long enough to realize they'd need to be calculated dynamically at course-creation time, not hardcoded into a chain of conditionals somewhere.

## Was tracking useful?
Tracking happened mostly through GitHub (issues closed, commit timestamps, pull requests merged). It was a decent sign for what got done, less useful for how long it actually took as tracking was inconsistent. Long debugging sessions didn't always get logged and some time spent reading documentation or iterating on prompts with Claude went unrecorded and needed to be estimated afterwards. 

## What should change?
A quick note when closing an issue would go a long way. Like "estimated X, took Y, here's why." Additionally, a plug-in to track coding time would have been extremely helpful due to an increase in accuracy. 

## AI use
Claude was used throughout the project. I used it most for problem-solving: describe the feature, share the relevant schema or component, ask what's wrong or how to structure it. Prompts got more specific as the project went on. Early ones were broad, something like "here's my Prisma schema, how should I model submissions?" Later ones were much more targeted, like "my clearTermApproval function isn't resetting points correctly, here's the transaction and what the DB looks like after running it."

Time breakdown per session was roughly five to ten minutes on prompt iteration, and fifteen to thirty minutes on verification and manual editing. Generated code almost always needed adjusting to match existing file conventions, handle edge cases the prompt didn't cover, or account for schema details Claude didn't have context on. 
