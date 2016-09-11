# Our Operating Process

## Iterations and Hours
We work on client projects in weekly iterations, four days per week. We typically work Monday through Thursday (barring no major holidays or staff illness). Fridays are normally reserved for echobind's internal business tasks. We work during normal business hours, but do not track the exact number of hours worked. All work that is completed during the week is clearly documented via source control, project management systems, chat and weekly recap meetings.

## Invoicing and Payment
We require one week's advance payment to begin a project. In successive working weeks, we invoice every Friday. Because we bill by the week, we do not itemize our invoices. We keep things simple for us and our clients and charge one amount per developer, per week.

Payment is due within 15 days of the invoice date. Invoices can be paid by check, wire transfer, or credit card.

## Communication
Slack is our preferred chat system. Each project receives a private chat room that brings together our developers and project stakeholders. This chat room is used to deliver all of our communications. We use Slack integrations extensively to notify us when important events occur.

Example events include:
- staging/production deployment notifications
- bug notifications
- source control commits
- project management updates

If you have files, documents, or images, you can drop them into the Slack chat room for group sharing. This practice eliminates cumbersome, back-and-forth processes such as sending multiple emails to several people or adding individual accounts to Dropbox shared folders.

In addition, we document our progress via GitHub (our preferred source control system) and Waffle (our preferred project management system). We put multiple processes in place so our clients never need to ask, "How is everything going?". We try to use chat as much as possible so we can communicate frequently and informally.

## Meetings

We don't have a lot of meetings. Our client’s budgets are far better served when we're actively working on a project. However, we do begin each project with a [Roadmapping Session](#the-roadmapping-session), which lasts between two hours and a full day. At the end of each week, we hold a quick recap meeting with our clients to discuss the iteration that was just completed. We limit the recap meeting to 30 minutes. Since we're a virtual office, we use Google Hangouts for the Roadmapping Session and the recap meetings.

## Project Management

Our preferred project management software is [Waffle](http://waffle.io). Waffle is a [Kanban board](http://en.wikipedia.org/wiki/Kanban_board) tool that integrates directly with Github Issues, which we use extensively during projects. These tools are easy to grasp and client friendly.

We usually set up our boards in the following way:

\vspace{14pt}

![waffle screenshot](source/waffle.png)\

\vspace{2pt}

As illustrated, features are first placed into the "Backlog" column. The client is expected to help write these features and review and suggest any necessary changes to them. Then, each week, we estimate which features can be completed and move them into the "Ready" column. While we do our absolute best to complete the "Ready" features within the week's iteration, we cannot guarantee that all work will be finished. Incomplete items from an iteration get moved to the next one. Once development or design work begins on "Ready" features, they are moved to "In Progress." Once completed, "In Progress" features are reviewed, and once they are accepted, items are marked as "Done.""  For more details about this process, see [Our Code Process](#our-code-process).

## The First Week
Our work in the first week can vary depending on the project's scope. But here are some of the things that we typically do:

- Conduct the Roadmapping Session with the client
- Set up any required accounts (hosting, source control, etc)
- Set up continuous integration (CI)
- Specify development process / workflows
- Audit existing code
- Write tests to cover untested functionality

## The Roadmapping Session

Before we begin working on a new project, we conduct a Roadmapping Session. During this meeting, we discuss the project and its relationship to the client's overall business. We also talk about use-cases, product validation, and the project's overall goals. This conversation enables us to produce a Roadmap, which is a 1 to 2 page PDF that details the project’s timeline and helps ensure its success:

\vspace{2pt}

![roadmap example](source/roadmap.png)\


## Maintenance Agreements

After completing a project, we can transition to a maintenance agreement. Maintenance agreements are billed as a monthly retainer and typically include:

- security updates and patches
- advice on best practices
- help architecting new features
- ongoing code review
- bug fixes

Maintenance agreements require a minimum three-month commitment and include up to 32 hours per month.

\vspace{14pt}

---
