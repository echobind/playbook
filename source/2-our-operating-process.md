# Our Operating Process

## Iterations and Hours
We work on client projects in weekly iterations, four days a week. We try to work work Monday through Thursday as much as possible. If there are holidays or someone gets sick, we will switch days around as best we can. We’re all pretty healthy people, so getting sick is rare.

We don’t track the exact number of hours worked during the week. We are open in our communication, and clearly document the work being done via source control and project management systems. You should never need to ask “how is everything going?” when working with us.

_keep this next one or no?_

While we generally keep normal business hours for the US Eastern timezone, we don’t strictly enforce it. On certain days, a developer may hit a stride at 8am. Or 6pm. Maybe a complicated algorithm is best worked out over a lunch time bike ride or a walk. We encourage these behaviors as it often produces the best work. Programming and designing are very intensive tasks and everyone needs to be fresh.

## Invoicing and Payment
We require payment for the first iteration to begin work on a project. Starting with the second week, invoices will automatically be sent out on Friday and payment is due within 15 days.

We do not itemize our invoices for the same reason we do not track exact hours. Weekly status is well documented by other means.

Invoices can be paid by check, wire transfer or credit card. 

## Communication
Slack is the chat system of choice for us. Each project gets a custom room that we use for all of our communication. We use Slack integrations extensively to give us notifications in the chat room when important events occur. 

Example events include:
- staging/production deployment notifications
- bug notifications

If clients have files, documents or images that should be included in the project, they can be dropped into the Slack chat room to be shared among everyone working on the project. This eliminates additional overhead like email or adding individual accounts to Dropbox shared folders.

## Meetings

We don’t have a lot of meetings. Everyone stays in communication using chat. The longest meeting we have is a [Roadmapping Session](#the-roadmapping-session), which is done at the start of the project. The length varies, but it can take anywhere from 2 hours to a full day.

Following the [Roadmapping Session](#the-roadmapping-session), we start off every day with a quick update on what’s going in our client projects, which usually takes 5 minutes or less.

At the end of a week we have a recap meeting to discuss the iteration that was just completed. If possible, we want our clients to attend this. We limit the recap meeting to 30 minutes.

We’re a virtual office, so we use Google Hangouts for both of these meetings. It’s nice to see everyone’s face.

## Project Management

Our preferred project management software is [Waffle](http://waffle.io). Waffle is a [Kanban board](http://en.wikipedia.org/wiki/Kanban_board) tool that integrates directly with Github Issues, which we use extensively during a project. Don’t worry if you’ve never used one of these types of tools; they are easy to grasp.

We typically set up our boards in the following way:

\vspace{14pt}

![waffle screenshot](http://echobind.s3.amazonaws.com/images/playbook/waffle.pdf)\

\vspace{2pt}

Features are placed into the “Backlog” column. At the start of each week, a certain number of stories are moved into the “Ready” column. This number is the estimated amount that can be done for the week. It is meant as a guide, not a hard number. If stories need clarification or modification, that should happen prior to moving the feature to “Ready”. When development or design work is started on a feature, the feature card is moved to “In Progress”. Items will automatically be marked as “Done” once the Pull Request is merged, a process that we detail in [Our Code Process](#our-code-process).

## The Initial Week
What we do in the first week varies widely depending on the project, but here are some of the things that we might do:

- The Roadmapping Session
- Account setup
- Set up CI (continuous integration)
- Help put development process / workflows in place
- Audit existing code to get a better grasp on what we’re dealing with.
- Write some tests to cover untested functionality

## The Roadmapping Session

The Roadmapping Session is one of the first things we do with clients. The product of this meeting is a visual Roadmap. The Roadmap is a 1 to 2 page PDF that maps out the project. We find that having something visual like this helps makes sure everyone is one the same page, and promotes quality right from the start. During the Roadmapping Session meeting, we discuss the relationship between your business and the project. We talk about use-cases, goals, how ideas have been validated, and many other things. We try do have the Roadmapping Session in person, but will use Google Hangouts if meeting in person is not feasible.

A hypothetical Roadmap might look like this:

\vspace{14pt}

![roadmap example](http://echobind.s3.amazonaws.com/images/playbook/roadmap.pdf)\

\vspace{2pt}

## Project Completion

We’re not the type of consulting company that just moves on to the next project. Having poured lots time and energy into a project, we want it to succeed. It’s not uncommon for us to use and promote a product we’ve worked on. Our ideal clients become long term partners. 

Our business thrives on referrals. During a project we’ll ask if you have any other contacts that we could help out. Having experienced how we work first hand, it would mean the world to us if you refer us to others.

## Maintenance Agreements

After completing a project, we can transition to a maintenance agreement. Maintenance agreements are billed as a monthly retainer, and typically include:

- security updates and patches
- act as an advisor on best practices
- act as an advisor when architecting new features
- ongoing code review / suggestions for your team
- bug fixes

Maintenance agreements require a minimum 3 month commitment and include up to 32 hours per month.

\vspace{14pt}

---