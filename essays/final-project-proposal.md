---
layout: essay
type: essay
title: "Final Project Proposal"
date: 2026-03-31
published: true
labels:
  - Software Engineering
  - Nextjs
---

<img width="200px" class="rounded float-start pe-4" src="../img/studyCircle.png">

## Project: KnowledgeVault

## Project: Study Guide

## Overview

**The problem:** Students struggle to access structured, verified study materials tailored to their specific courses. Each discipline has different learning needs—some courses require mastering terminology, others need worked problem solutions, analyses, or conceptual frameworks. Currently, students piece together study resources from scattered sources (textbooks, lecture notes, online forums) without quality assurance or institutional support. Additionally, students don't know what to expect from a course before enrolling.

**The solution:** Study Guide is a collaborative platform where instructors define what study materials their course needs, and students earn extra credit by submitting, reviewing, and refining those materials. All approved submissions compile into comprehensive, interactive study resources organized by topic. By enabling cross-course sharing and open resource exports, Study Guide becomes a community-driven resource that benefits current and future students across disciplines.

## Approach

Study Guide has three main user roles: students, instructors, and teaching assistants (TAs). Any user can have multiple roles (for example, a graduate student can be both a TA and a student in a different course).

**Instructors** create course study material structures by defining what types of content their course needs (starting with glossary terms in Phase 1). They set extra credit point values for contributions, control whether students can access previous semester materials, and export compiled resources as open educational resources.

**Teaching Assistants (TAs)** select the highest-quality student submissions and approve them for the glossary. They can view and provide feedback on the selection process.

**Students** enroll in courses, view study materials, and strategically submit content for assigned course topics. Students earn extra credit for having their submission selected as the approved glossary entry. They study interactively by highlighting, annotating, and bookmarking materials. If the instructor allows, students can access previous semester materials to understand course expectations before enrolling.

## Phase 1: Glossary-Based Study Materials (MVP)

For the initial implementation, Study Guide focuses on **terminology and definitions**—a foundational content type that works across most disciplines.

**Instructor-Defined Glossaries:**
- Instructor adds terms for each week or topic
- Optionally marks terms as requiring visual annotation
- Provides optional reference definitions or context

**Student Submissions & Competition:**
- Students can submit definitions for glossary terms
- **Per-Student Limit:** Each student can submit 1 definition per week maximum
- **Per-Term Cap (based on class size):** Each term can receive multiple submissions for competition:
  - 1-20 students: 3 submissions per term max
  - 21-40 students: 4 submissions per term max
  - 41+ students: 5 submissions per term max
- Once a term reaches its submission cap, no more submissions are accepted for that term that week
- This creates strategic choice: students must decide which terms to attempt based on difficulty, competition level, and their strengths
- Ensures all glossary terms receive attention and have quality submissions to choose from

**Submission Content:**
- Text definition written in the student's own words
- Optional: Upload visual annotations (labeled diagrams, sketches, annotated images)
- Optional: Add examples or relate to other terms
- Designate difficulty level (Basic / Intermediate / Advanced)

**Competitive Review & Approval Process:**
- All submissions are visible to the class as reference materials
- **TA/Instructor selects the highest-quality submission** based on:
  - Accuracy and completeness
  - Clarity and pedagogical value
  - Visual annotations quality (if applicable)
  - Overall helpfulness as a study resource
- Only the approved submission is added to the official glossary
- Only the student whose definition was selected earns extra credit (3-5 points typical, varies by quality)
- Other submissions remain visible as supplementary resources but don't earn credit, allowing students to learn from multiple approaches

**Interactive Study Features:**
- Highlight key phrases (color-coded for personal use)
- Add private annotations to any term
- Bookmark important terms
- Create custom study sets
- Use flashcard study mode
- Search and filter by week, difficulty, or content type
- View multiple submitted definitions (approved and unapproved) to understand different approaches

## Mockup Page Ideas

Some possible mockup pages include:

- Landing Page / Home Page
- Login / Register (with role selection: student, instructor, TA)
- Student Dashboard
- Instructor Dashboard
- TA Dashboard
- Course Study Resource View
- Glossary Term View (showing all submissions and ratings)
- Student Submission Form (text + image upload)
- TA Selection Interface (choosing the best submission)
- Interactive Study Material (with highlighting and annotation tools)
- Previous Semester Materials View
- Student Profile (submission history, extra credit balance)
- Resource Export Modal
- Course Analytics Page

## Use Case Ideas

Whether or not the following bullet points list all pages or not, the completed use case should show an end-to-end scenario of using the system.

1. New student logs in, enrolls in Anatomy 141, reviews the previous semester's glossary (if enabled by instructor) to understand the terminology load and course expectations, and feels more prepared for the course.

2. Instructor creates Anatomy 141 course, adds weekly glossaries with terms like "cranial nerves," "neurovascular," and "thorax," sets extra credit values (3-5 points per approved definition), and enables access to previous semester's glossary from Day 1.

3. Week 1 releases 5 glossary terms. Student A wants to submit a definition but sees "neurovascular" is the most straightforward. However, it already has a submission. Student A chooses to tackle "cranial nerves" instead, submitting a detailed definition with a labeled diagram.

4. Student B also submits a definition for "cranial nerves" before the submission cap closes. Both definitions are visible to the class.

5. Student B's submission remains visible as a supplementary resource. Student B can see the feedback and learn from the comparison.

6. Student opens the compiled Anatomy glossary, highlights "cranial nerves" in yellow, adds personal note "Remember: 12 pairs, some sensory only," bookmarks "neurovascular" for later review, and uses flashcard study mode the night before the exam.

7. End of semester: All approved glossaries compile into a final Anatomy 141 Master Glossary. Instructor exports the glossary as a PDF study guide, an Anki flashcard deck, and a Markdown file shared on GitHub under Creative Commons license.

8. Next semester, Anatomy 141 (Section B) is taught by a different instructor. Study Guide links the previous semester's glossary as a starting point. New students and instructors build upon and refine the existing glossary, creating a continuously improving campus resource.

9. Student previews Anatomy 141 glossary before enrolling, sees the terminology load and existing resources, and decides to enroll confidently knowing what to expect.

## Beyond the Basics

After implementing the glossary-based MVP, here are ideas for more advanced features:

### Interactive Study Features (Phase 2):
- Study progress tracking and personalized reports
- Flashcard integration with Quizlet, Memrise, and other apps
- Accessibility features (alt-text generation, text-to-speech)
- Mobile app or progressive web app (PWA)

### Cross-Course & Resource Sharing (Phase 2):
- Cross-course glossary linking (multiple sections build shared master glossary)
- Open resource export (PDF, Markdown, Anki format with Creative Commons licensing)
- Featured glossaries on homepage (showcase best course resources)

### Extending Content Type (Phase 3+):

The system is designed to scale beyond glossaries to support multiple content types per course. Instructors could eventually define what their specific course needs:

**Example Content Types (Future Expansion):**
- **Worked Problem Solutions** (Math, Physics, Chemistry): Students submit step-by-step solutions with explanations
- **Code Examples & Snippets** (Computer Science): Students submit annotated code with explanations of functionality
- **Conceptual Analyses** (Literature, History, Philosophy): Students submit essays, character analyses, thematic breakdowns
- **Lab Procedures & Reports** (Biology, Chemistry): Students submit lab protocols, data interpretations, experimental summaries
- **Grammar & Usage Examples** (Languages): Students submit grammar rules with example sentences and contextual usage
- **Case Study Analyses** (Business, Law, Medicine): Students submit detailed case analyses with critical thinking

**How This Works:**
1. Instructor selects content types for their course (or creates custom ones)
2. Instructor provides submission templates/rubrics for each type
3. Students submit according to templates
4. Peer ratings and TA selection process work the same way
5. Materials compile into tailored study resources

## Team Members

This proposal was created as a collaborative effort by the authors.
