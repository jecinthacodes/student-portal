# EduFlow — CSC 1/4 Student Portal

**A single-page student portal built for the University of Cross River State (UNICROSS) Computer Science Class of 2026, Set 1/4.**

Live demo: [jecinthacodes.github.io/student-portal](https://jecinthacodes.github.io/student-portal/)

---

## Overview

EduFlow is a front-end web application designed to centralize the everyday information a first-year Computer Science class needs to stay coordinated: class schedules, announcements, class representative contacts, and a bird's-eye view of the four-year degree programme. It was built to replace the scattered mix of WhatsApp broadcasts, printed timetables, and word-of-mouth updates that most Nigerian university classes rely on, by giving CSC 1/4 a single, always-available reference point.

The portal is intentionally scoped to one class (CSC 1/4, 2025/2026 session) rather than being a general-purpose institutional system — it models real data for that class: 398 students, 7 registered courses, and a two-semester academic calendar.

## Core Features

### 1. Authentication Gate
A sign-in screen requiring a registration number and password (default password = registration number), styled as the entry point to the portal. This establishes the pattern for future access control, even if the current deployment is primarily informational/static.

### 2. Dashboard / Home
- Live counters for total students (398) and courses (7)
- A "Next Lecture" widget showing the soonest upcoming class with time, venue, and course code
- Quick navigation into Announcements, Class Reps, and Schedule sections

### 3. Course Schedule
A filterable weekly timetable (All / Mon / Tue / Wed / Thu / Fri) covering all 7 courses:

| Code | Course | Units | Day(s) | Time | Venue |
|------|--------|-------|--------|------|-------|
| MTH 101 | Mathematics I — Algebra & Calculus | 3 | Mon, Thu | 10:00–12:00 | Room 204, Block B |
| PHY 101 | Physics I — Mechanics & Waves | 3 | Tue, Fri | 8:00–10:00 | Physics Hall, Block C |
| COS 101 | Introduction to Computer Science | 2 | Wed | 8:00–10:00 | Main Hall, Block A |
| CSC 181 | Computer Science Laboratory | 1 | Tue | 14:00–16:00 | Lab A, ICT Centre |
| STA 111 | Introduction to Statistics | 3 | Mon, Wed | 12:00–14:00 | Room 301, Block D |
| PHY 107 | Physics Lab — Practical Sessions | 1 | Fri | 10:00–13:00 | Physics Lab, Block C |
| GST 111 | Communication in English | 2 | Thu | 14:00–16:00 | Arts Hall, Block E |

**Total: 15 credit units**, across a day-by-day breakdown (Monday–Friday) as well as a full weekly grid view.

### 4. Announcements
A feed of pinned and time-stamped class updates (exam schedules, assignment reminders, lab reschedules), each expandable into a full detail view. Announcements carry metadata tags (e.g. "Important," "Rescheduled") for quick scanning.

### 5. Class Representatives
Profile cards for the Class Rep and Assistant Rep, including registration numbers and (in the expanded view) responsibilities and contact information — the designated points of contact for portal issues or class matters.

### 6. Upcoming Events
A running list of the next deadlines and events (assignment due dates, tests, exams, project submissions) with type tags (Assignment / Test / Exam / Project) and dates.

### 7. Programme Roadmap
A four-year progression view (100L → 400L) showing where the current class stands (Year 1 of 4, 25% complete) and what each subsequent year covers — foundation courses now, core CS in Year 2, advanced CS in Year 3, and AI/final-year project/industrial training in Year 4.

### 8. Semester Timeline
Session metadata: semester dates, mid-semester exam date, end-of-semester date, and total week count (15 weeks), giving students a persistent sense of "where we are" in the term.

## Technical Notes

- **Architecture:** Single-page application (SPA) pattern — in-page navigation via anchor links (`#home`, `#announcements`, `#reps`, `#schedule`) rather than separate page loads, with detail views ("Back to Portal") layered on top of list views.
- **Hosting:** Deployed via GitHub Pages directly from the repository.
- **Design approach:** Card-based, dashboard-style UI with stat counters, tag-based filtering, and a consistent "back" navigation pattern for drill-down views (announcement detail, rep profile, course info).
- **Data model:** Currently static/hardcoded to CSC 1/4's actual 2025/2026 schedule and roster — a natural next step would be externalizing this into a JSON/API layer for reuse by other classes or sessions.

## Why This Project

University departments in many Nigerian institutions don't provide digital portals down to the class level — students are left to self-organize. EduFlow demonstrates how a class of ~400 students can maintain a shared, structured source of truth using nothing more than static web technologies and free hosting, while still covering the features a heavier, database-backed system would offer: auth, scheduling, announcements, and role-based contacts (class reps).

## Roadmap / Possible Extensions

- [ ] Replace hardcoded data with a JSON or lightweight backend data source
- [ ] Real authentication (currently a UI pattern, not enforced access control)
- [ ] Push/email notifications for new announcements
- [ ] Assignment submission tracking
- [ ] Mobile-first responsive polish
- [ ] Multi-class / multi-session support

## Credits

Designed and built by **Jecintha** (with portal design credit noted to **Nworah, C.J.** in the site footer), for CSC 1/4, UNICROSS, 2025/2026 session.

---

*This README was expanded to give visitors and collaborators full context on the project's scope, data model, and feature set beyond a one-line description.*
