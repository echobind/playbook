# Our Operating Process

## Iterations and Hours
We work on client projects in weekly iterations, four days a week. We try to work work Monday through Thursday as much as possible. If there are holidays or someone gets sick, we will switch days around as best we can. We’re all pretty healthy people, so getting sick is rare.

We don’t track the exact number of hours worked during the week. We are open in our communication, and clearly document the work being done via source control and project management systems. You should never need to ask “how is everything going?” when working with us.

_keep this next one or no?_

While we generally keep normal business hours for the US Eastern timezone, we don’t strictly enforce it. On certain days, a developer may hit a stride at 8am. Or 6pm. Maybe a complicated algorithm is best worked out over a lunch time bike ride or a walk. We encourage these behaviors as it often produces the best work. Programming and designing are very intensive tasks and everyone needs to be fresh.

## Invoicing and Payment
We require payment for the first iteration to begin work on a project. Starting with the second week, invoices will automatically be sent out on Friday and payment is due within 15 days.

We do not itemize our invoices for the same reason we do not track exact hours. Weekly status is well documented through other means.

Invoices can be paid by check, wire transfer or credit card. 

## Communication
Slack is the chat system of choice for us. Each project gets a custom room that we use for all of our communication. We use Slack integrations extensively to give us notifications in the chat room when important events occur. Example events include:

- staging/production deployment notifications
- bug notifications

If clients have files, documents or images that should be included in the project, they can be dropped into the slack chat room to be shared among everyone working on the project. This eliminates additional overhead like email or adding individual accounts to Dropbox shared folders.

## Meetings

We don’t have a lot of meetings. Everyone stays in communication using chat. We start off every day with a quick update on what’s going in our client projects, which usually takes 5 minutes or less.

At the end of a week we have a recap meeting to discuss the iteration that was just completed. If possible, we want our clients to attend this. We limit the recap meeting to 30 minutes.

We use Google Hangouts for both of these meetings since its nice to see everyone face-to-face.

## Project Management

Our preferred project management software is Waffle. Waffle is a [Kanban board](http://en.wikipedia.org/wiki/Kanban_board) tool that integrates directly with Github Issues, which we use extensively during a project.

We typically set up our boards in the following way:

\vspace{14pt}

![waffle screenshot](http://echobind.s3.amazonaws.com/waffle.png)\

\vspace{2pt}

Features are decided on and put into the “Backlog” column. At the start of each week, the project manager will move a certain number of stories into the “Ready” column. This number is the estimated amount that can be done for the week. It is meant as a guide, not a hard number. As development or design work is started on a feature, the feature card is moved to “In Progres”. With Waffle, items will automatically be marked as “Done” once the Pull Request is merged, a process that we detail in “Our Code Process”.


---