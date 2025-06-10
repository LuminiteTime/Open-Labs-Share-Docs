## Project Description
---

***Open Labs Share*** is a peer-to-peer educational platform that connects experts with learners through hands-on, practical learning experiences. Here's what it offers:

- **Expert-Created Content**: Subject-matter experts design step-by-step lab exercises focused on real-world applications
- **Practical Learning**: Students complete these labs to develop skills they can immediately apply in professional settings
- **Community Feedback**: A peer review system where learners evaluate and provide feedback on each other's completed assignments
- **Knowledge Sharing Ecosystem**: A collaborative environment where practical knowledge is actively exchanged among community members

Essentially, it's like combining the practical approach of a university lab with the collaborative feedback of platforms like GitHub or Stack Overflow.

## Competitive Advantages
- **Practical Focus**: Emphasis on real-world application sets it apart from theory-heavy platforms
- **Peer Review System**: Creates engagement and community while reducing expert workload
- **Expert Monetization**: Attractive proposition for subject-matter experts to share knowledge profitably


## Project Analysis
---

### Key features:
- Publishing lab materials (Markdown document with assets)
- Submitting finished work in PDF format.
- Ability to leave feedback on somebody's work

#### Publishing lab materials
Lab materials are represented in web page as rendered Markdown documents with exact practice topic. When upload a new lab, user should send main Markdown document with all required assets (image files) names exactly as they are referred in document.
Each lab should be a list of steps required to do / create / build something. All labs should be practically oriented. Consequently, each lab should have afterward hands-on exercises (theoretical questions, practical tasks).

#### Submits of homework
Each student must be able to do a homework (set of exercises) after the lab. In order to have feedback, student may submit a finished work in **PDF** format to a platform. Each submission is connected to the exact lab and its set of exercises. 

#### Submit evaluating
The author of the lab or people that have finished the lab should be able to check new homeworks from other people.

> [!note] User story on submit evaluation
> **As a** lab author or student who completed a lab 
> **I want to** review and provide feedback on submitted homework 
> **So that** I can help other learners improve their practical skills and contribute to the learning community
> 
> **Acceptance Criteria**:
> 1. GIVEN I'm on the control panel, WHEN I click "Review Submissions", THEN I see labs I'm eligible to review with submission counts (I see the cards of labs I have already submitted and number of available homeworks under each title.)
> 2. GIVEN I select a specific lab, WHEN I view available submissions as cards, THEN I see homework cards with student name, submission date, and title
> 3. GIVEN I click "Review Submission" button placed on submission card, WHEN the review interface opens, THEN I see the PDF rendered clearly with a feedback form alongside (on the right)
> 4. GIVEN I'm writing feedback, WHEN I submit my review, THEN the student receives notification and I see confirmation
> 5. GIVEN there are no submissions available, WHEN I access the review section, THEN I see a helpful message explaining the situation

## Features prioritization
---

### MVP must have features

Users should be able to:
- Create personal account
- Publish labs
- Read labs
- Submit homework for labs
- Review and leave feedback for lab submits

### Extra features
- Lab categorization
- Lab search by title, categories
- Lab feedback (simple feedback with comment and scores)
- Test questions with auto check after lab
- Submit review with form (standardized feedback form)

## Monetization
---
- **Courses**
	Teachers can create paid courses. When students are enrolled, owner of the course get money from them, but part of this money goes to our service.
- **Ads** 
	After reaching some threshold with reputation, partnership program is available. Labs' authors pay, our service promote these users and their courses via ads.
- **AI** 
	Paid AI service. First tries are free, then pay.
- **Paid access to labs**
	Membership program. Paid subscription allows for publishing special labs which can be accessed only by another members of the paid subscription. (see Medium).
- 