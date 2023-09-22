---
title: "Other Requirements"
date: 2021-05-28T09:44:45-05:00
draft: false
layout: page
---

This page is intended to lay out the basic “rules and requirements” that our organization requires of all Summer of Code (whether GSoC or SOCIS) participants whose project proposals are accepted. Unless otherwise arranged with the organization administrator, it will be expected that all students will comply with the requirements outlined below.

### Application Recommendations
**Make a patch**:
While this is optional, it greatly increase your chances of being selected. Basically, a patch is some change to the software (submitted either as a patch file or a pull request). If working with us is your top priority, a patch will help us see how well you are at dealing with other people's code. Don't worry, though. It doesn't need to be more than a few lines. It can be a bug fix or implement some minor feature. It's more important that it applies without hassle and provides some improvement. This is one of several opportunities to impress, so be creative. Link to any patches in your application.

**Come talk to us**:
You really should be talking to developers long before you submit an application. Discuss your ideas via Gitter and Github. Communication is a huge part of our evaluation criteria.

**Maintain a dev log**:
It's strongly recommended that you maintain a public development log that is updated every day you work. Most students don't have a habit of discussing their work adequately and this intrinsically documents progress. Communication ftw. Dev logs are also a great way to let people in the community follow your project and provides a place to showcase cool highlights!

### Participation Requirements
**License appropriately**:
Participation requires that any work performed will be provided in good faith and consistent with contributor requirements. Unless approved in advance in writing, all rights (copyright) will be assigned to the organization. If your country does not allow assignment of copyright, non-exclusive rights to use the code in perpetuity will be required. You will be credited for your work regardless.

**Report activity daily**:
In addition to your ongoing discussions, it is required to regularly submit a progress report of daily activity. These reports usually won't need to be more than a sentence or two but they should provide clear concise information on what you did, things you discovered, tasks completed, difficulties encountered, milestones reached, days off, and other similar details. If you did nothing, that's okay! We want to know when you're concentrating on code, at the beach, and everything in between.

**List your milestones**:
Everyone is required to submit a minimum of three and a maximum of ten project milestones. These are not deliverables but, rather, are overall tasks that should be completed throughout the duration of your work. These should be necessary implementation steps and not include any research or familiarity phases. In the end, there is code that must be produced and your milestones should be a (very) rough breakdown for estimating your progress. These milestones should be published in your first progress report, that is, at the beginning of coding.

**Be communicative**:
All students will be expected to be reachable via Gitter and e-mail while they are working. Participants must be responsive, actively engaged in discussions, and available for questions, comments, and suggestions from other developers. See here if you are new to Gitter and need help.

### Coding Requirements
**Compile and run**:
Being able to compile and run on your own hardware is a very basic task that is considered essential. We're more than happy to help you get started the first time if you run into a problem, but you are expected to put forth duly diligent effort. Additionally, understanding the existing user community is very important for most developers to have at least a basic familiarity. In the end, your changes will (hopefully) be pushed out to the community and you should be cognizant of what that will mean.

**Be familiar with revision control**:
You will be expected to abide by the same coding requirements of other developers. You must know the basics for how to work with the project's revision control system including checking out/in changes, resolving conflicts, and creating patches. Whether you work on a branch or on the mainline trunk will depend on the project.

**Evaluate performance**:
Performance is something we always strive to keep in mind. Quantitatively evaluate your performance and the impact your modifications will make. Don't prematurely optimize and don't over-architect, but also don't make guesses or assumptions either. Use a performance profiler, test your code, add debug timers, and/or have a peer review your work.

**Write maintainable code**:
This requirement cannot be stressed enough. How maintainable is your end result. This is not only maintainability from the stand-point of source code longevity, but involves other higher-level aspects. Does your implementation use interfaces, languages, tools, or techniques that introduce some new development requirement? If so, that choice needs to be discussed and justified or otherwise mitigated. Any new external dependencies need to be approved by the core developers. Is your code comprehensive and comprehensible? Well-documented? Organized? You are required to follow existing dev guidelines, code style, and established conventions.

**Write portable code**:
We appreciate code being as portable as possible with effort continually taken to make sure code works on a variety of environments. While each developer's perception of what is reasonable certainly fluctuates over the years and from developer to developer, the general intention is that code written should function the same on most moderately popular operating system environments. It is each dev's responsibility to either make sure their code isn't platform-specific or that equivalent functionality is implemented for other maintained platforms. You are expected to interact with other devs when portability issues are raised and to promptly resolve any problems. Portability of any dependencies being used must similarly be taken into account and relates to the aforementioned maintainability requirement.

**Write complete code**:
Perhaps treat each week like it is your last. You should be able to hand over functional code over just about any time during development (within a day or so) to another developer. Focus on completing tasks, completing code features, and working on keeping your code functional at all stages of development. That way, no matter how far you get on your milestones or deliverable(s), other developers will be able to review, test, and readily integrate your code. Plan your development approach accordingly. You should generally not “stub” code functionality (though comments are good), but instead focus on coding “deep” instead of “wide”. It's generally preferred to have 2 features that work fully, than 5 features that half-work or even 20 features that are all 90% complete.

# Application Guidelines

### Writing a Successful Application
Students should propose what they actually intend to accomplish, what they know about that task, and details about their background. Ability to perform the task is outright presumed by submitting a proposal. Students should propose a project catered to their ability that can be completed within the timeframe of the program. Students can demonstrate coding experience with patches.

Early submissions are encouraged as it gives more time to review proposals in detail, offer feedback, and maybe ask questions. Submitting closer to the deadline isn't bad other than not getting feedback in advance.

### Do
**Be Detailed and Articulate**: Go into detail about what you intend to do and how you intend to do it. Don't have typos and be clear in your writing. Cite academic references if they're relevant to your work. Create diagrams, show prototypes, create mock-up visuals, and provide more information via external links. You don't have to solve everything, but we need to see that you've thought things through.

**Get Involved Early**: Join Gitter, say hi on the mailing list, download the source code, and try things out. Talk to others, get to know who is who. Communicate early, communicate often.

**Be Bold**: We love innovative ideas. Make sure yours is in scope and is something we're interested in mentoring, but you're not limited to our ideas. Be ambitious and thorough in your solution.

**Be Realistic**: Make sure the scope of your work is feasible and that you will have the necessary skills to implement your project on time. No bonus for proposing to reinvent the Internet. If you've got another job or commitment, your proposal should account for that obligation.

**Be Passionate**: Show enthusiasm for your idea. Be excited. Passion is never a substitute for competence, but vastly helps your chances all other factors being equal.

### Avoid
**Don't copy/paste**: If all you have to say about the project idea is what we wrote, it will be rejected. They are just meant to be starting points.

**Don't be brief**: Anticipate questions, include details. If your application is less than a few hundred words, you're probably not including necessary detail about your plans or yourself. Brief proposals very quickly get cut.

**Don't be intimidated**: We don't bite. Your ideas will be questioned, we might disagree, and that's okay. It means we're interested. You will need to be able to talk about your ideas without getting defensive, be open to compromise, and take suggestions from others.

**Don't be discouraged**: We have accepted those with no experience to experts and everything in between. Cater your application to your skills and you'll do just fine. You're expected to work hard and do your homework researching questions, but you're encouraged ask for help if you truly get stuck too.

**Don't forget to tell us about yourself**: Most of what we know about you and your abilities is going to come from your application. Include details about your background, experience, and anything else relevant to your work. If you have obligations that will impact your proposal, be upfront. You should be interacting with our community on Gitter or on the developer mailing list long before you submit your proposal so we have an idea how you interact. Don't forget to mention your Gitter/GitHub nick in your application.

### Application Format
There is intentionally no specific format to our applications. **BUT**... students are **strongly** encouraged to be creative, detailed, and discuss throughout the application process. Use a wiki page or the mailing list so your proposal can be reviewed before it's officially submitted. Final proposals should include **at least** the following information:

1. **Personal Information**
   - Name
   - Email address
   - Github username
   - Brief background info
   - (optional) Link to resume
2. **Project Information**
   - Project Title
   - Brief project summary (<500 words)
   - Detailed project description (>500 words)
   - Links to any code or algorithms you intend to use
   - Deliverables (specific, measurable goals)
   - Development schedule, list at least 3 milestones
   - Describe time availability (40+ hours/week assumed), list all commitments (e.g., exams, vacations, etc)
   - (optional) Why us?
   - (optional) Why you?
   - (optional) Anything else?

**You must agree to our [acceptance requirements](../requirements) should you be selected.**

# Participation Expectations


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

We also abide by the Astropy Community Code of Conduct and if there are any violations students should email <a href="mailto:tardis.supernova.code@gmail.com">tardis.supernova.code@gmail.com</a> to arrange for a confidential meeting.

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