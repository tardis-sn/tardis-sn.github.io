---
title: "Participation Expectations"
date: 2021-05-28T09:44:45-05:00
draft: false
layout: page
---

Covered below in detail are the expectations for Summer of Code students that are accepted to participate. In addition to the [acceptance requirements](../requirements) that all students are required to abide by, there are participation and behavior expectations.

The program timeframe is very **short**. There's not much time to get up to speed, so there is a need to be clear of what is expected. Also, many students haven't done a lot of real-world development work previously. On top of that, most mentors and students are in different locations so coordinated interaction can be difficult at times. Because of this, it's vitally important to the success of each student's project for all expectations to be specified and understood before students begin coding for the summer. This should be the first step in a long series of frequent communication between student and their mentor(s).

This document walks through various expectations for students and mentors, as well as addressing various ways to communicate effectively.

### The Point
One of the primary purposes of the program is to introduce students to real-world open source development where there are social, collaboration, and other pragmatic concerns in addition to technical implementation issues. It is our goal to integrate all participants as full-fledged new developers on the project not just for the duration of summer but thereafter too. The projects are a very important part of the program, but they're certainly not the most important part. The point is to have new developers join in development.

### Full-time effort
Unless otherwise discussed, students are expected to work about 40 hours a week on their project. This is essentially a full-time job. If students can't work this much or if there are periods of time when a student will be away on vacation, then that needs to be discussed beforehand with the mentors or project administrator. The mentors shouldn't have to hunt you down to keep tabs on your activity either (see Version control below).

### Self-motivation and steady schedule
The student is expected to be self-motivated. The mentor may push the student to excel but if the student is not self-motivated to work, then the student probably won't get much out of participating. The mentors are there to help, but they're not supposed to be a crutch or substitute for research and hard work. The student should schedule time to work on the project each day and keep to a regular schedule. It's not acceptable to fiddle around for days on end and then pull an all-nighter just before deadlines. It will show in code and in the evaluation.

### Integrated development
This means that students should be working closely with the other developers. Particularly for new projects, students are expected to keep up-to-date and deal with the on-going developments of others (both good and bad) just like any other developer on the project and is conscious of making changes that might break protocol or compatibility. You're not an outsider. You're joining a team.

### Version control
A developer has the responsibility to work cooperatively with the other developers. Particularly for open source projects, the manner in which everyone commits conveys a lot of information about the status, purpose, and directions of development.

#### Do
1. **Commit early, commit often.** This allows issues to be caught quickly and prevents the dreaded one-massive-commit-before-deadline. Developers can rarely ever commit too frequently. They can very easily commit too infrequently. Once a day is far too infrequent.
2. **Use quality commit messages.** The history in version control is frequently the best timeline log of what happened, why, and who did it. The commit messages should be detailed and informative.
3. Bad examples- 
   - "Fixed a bug"
   - "Tweaks"
   - "Improved version"
  
#### Avoid
1. **Checking in multiple non-related changes in one big commit.** If something is bad about one of the changes and someone needs to roll it back, it's more difficult to do so. Make each commits succinct and functional, even if it means a little extra work.
2. **Checking in changes that haven't been tested.** Each commit should at least compile for the person that makes the commit. New developers that break the build are used for target practice.

### Frequent communication with mentor
Frequent communication with your mentor is a must. The student should make sure the mentor has a good idea of: what you're currently working on.
1. How far you've gotten
2. How you're implementing it
3. What you plan on working on next
4. What issues have come up
5. What you did to get around them
6. What's blocking you if you're stuck
   
The mentor is one of the most valuable resources to students. The mentors are generally already solid contributors with a long track record of involvement with the project. The mentor likely has worked on the project for long enough to know the history of decisions, how things are architected, the other people involved, the process for doing things, and all other cultural lore that will help the student be most successful.

Before coding begins, the mentor and student should iron out answers to the following questions: 
1. What is the communication schedule? Daily? Every two days? Mondays, Wednesdays, Fridays? 
2. What is the best medium to use for regular, scheduled communication? IRC/Gitter? Mailing list e-mails? Instant messenger? VOIP? Telephone call? Face-to-face? 
3. What is the best medium to use for non-scheduled communication? IRC/Gitter? Mailing list e-mails?

#### Do
1. Keep your mentor up to date as much as possible. This forces you to be more organized and it gives your mentor a chance to help you out if you're having trouble.
2. Let your mentor know what your schedule is. Are you going on vacation, moving, writing papers for class? If your mentor doesn't know where you'll be or to expect a lag in your productivity, your mentor can't help you course correct or plan accordingly.

#### Avoid
1. Going for more than a week without communicating with your mentor. The project timeline doesn't allow for unplanned gaps in communication. Students should talk to their mentor at least once a week to update them on their status whether the mentor asks for it or not.

### Communication with project
**Students should not discuss development in private.** This includes refraining from private IRC/Gitter discussions as well as private e-mails even with your mentor unless the discussion involves personal information. Other developers need to be aware of the progress, discussions, and decisions being made even if they're not a part of that process. It also affords other developers the opportunity to get involved if they have an interest. Don't be shy, speak up publicly.

### Gitter
Students should be available via Gitter while they are working. This allows for interactive discussions with other developers and other students as well as increased visibility.


### GitHub
Many of the mentors may not be available on Gitter due to differences in time zones or familiarity with Gitter as a communication medium. Students should get to know their mentor and if GitHub discussions are preferred, the students should also be interactive and visible on the developer mailing list.

### Resolving problems
Student can call upon any mentor or other developer, they don't have to limit their interactions to just their mentor. They shouldn't limit their interactions to just one mentor. Students having difficulties communicating with any mentor should contact the <<email_kerzendorf>>.

We also abide by the Astropy Community Code of Conduct and if there are any violations students should contact <<email_kerzendorf>> to arrange for a confidential meeting.

If you're stuck, ask for help on Gitter and/or on the mailing list. If you are still stuck, read the source code. If you're still stuck, ask for help again. Better questions frequently yield better answers.

### Design documents
It's a good idea for the student to maintain design documents during the course of development. These design documents should cover: 
1. The project plan, with additional detail to flesh out the original program application 
2. Deviations from the project plan and how and why the original design plan changed 
3. Any issues that could not be worked out or overcome 
4. Possible future directions 
5. Any resources used or relevant specifications

The student and mentor should work out what design document(s) should be maintained during the course of the summer. The design documents should be added to the wiki.

_Thank you to each student for doing your best to follow through with these expectations. Students should consult with any mentor if there are any questions or concerns regarding these expectations._

_Many thanks to the Python foundation for their initial write-up document on participant expectations: http://wiki.python.org/moin/SummerOfCode/Expectations_