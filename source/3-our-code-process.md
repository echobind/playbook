
# Our Code Process

## Source Control
We use GitHub to host the source code for all of our projects. Github provides workflow features that are a core part of our development and design process. If the client requires that source code be managed in-house, GitHub offers an Enterprise Edition.

## Frameworks
We use ember.js for the front-end of our apps and Rails for the back-end code and API. Both of these frameworks promote convention over configuration. They operate in a similar way and work really well together. However, occasionally, we use Rails for the front-end in cases where we can’t use Ember.

## Development Workflow
We follow a standard branching workflow during development:

1. A developer **creates a branch** from master that describes the feature. The branch is prefixed with the developer initials. Example: 'cb-allow-users-to-order-takeout'
1. During development, the branch should be periodically pushed to origin. When the code is complete with **tests written to back up the change**, the developer looks through the commit messages in the branch and makes sure that they are readable and understandable. Any commit messages that need to be updated are fixed using the interactive rebase feature of git. 
1. The developer **creates a Pull Request** on GitHub. Slack notifies the team. We require all Pull Requests to be reviewed and marked with a +1 by another team member. This marking indicates that the changes are ready to merge to master.
1. When the Pull Request is opened, **a CI (Continuous Integration) server runs the test suite**, ensuring the entire test suite still passes. The CI server will automatically update the Pull Request with the pass/fail status of the test suite.
1. If a Pull Request has a +1 and passes CI, it is **merged to master** by the developer who originally opened it. 
1. The CI server will run the test suite a final time, and **automatically deploy to a staging server** where it can be reviewed from the browser.
1. After a merge, developers should spot check the feature on the staging server so they can be sure everything works as intended in a production-like environment.

## More on Continuous Integration
Testing Automation from a CI server is vital to our process. Testing Automation ensures our developers write proper tests, and it prevents changes to the app from “breaking” the test suite. The CI server is connected to Slack and notifies us if a Pull Request is ready to merge. Once merged, the CI server auto-deploys to staging. Codeship is our preferred CI server because it’s easy to use, supports multiple languages and test suites, and is reasonably priced.

## Releasing to Staging
We auto-deploy to a staging server so that it always reflects master. This deploy serves as the final gate check before code is released to production.

## Releasing to Production
We release code to production by either: (1) manually deploying through a script or git push; or (2) using the promote feature available on certain hosts. All of our developers can deploy to production, and they typically do so multiple times per day.

## Databases
Postgres is our database of choice. Postgres is proven, reliable, and modern.

We recommend that our clients migrate to Postgres if they use Mongo to store their data. We can complete this migration for you. In our experience, Mongo is often used to store data in a relational manor, a purpose for which it was not designed. As a result, it performs poorly. We’ve even seen cases where Mongo has caused our clients to lose data. Mongo does not support transactions or rollback features. For these reasons, we have instituted a “No Long-term Mongo” policy on all new projects.

## Code Quality
We value code quality. Code that is easily readable and cleanly written is easier to maintain and update in the future. 

We use Code Climate along with code reviews in Pull Requests to help us maintain code quality.

We aim for about 80%  test coverage on projects. We’ve found that striving for a very high percentage offers diminishing returns, and can cause developers to write bad or unnecessary tests. Instead, we rely on our developers to write enough tests to be confident that the project is sufficiently covered.

## Code Style
For Ruby code, we follow a [community style guide](https://github.com/bbatsov/ruby-style-guide) with a few minor additions:

- We allow omission of parenthesis when calling methods, e.g.: `User.eat 'taco'` and `User.eat('taco')` are both acceptable.

We are working on a style guide for our Ember applications.

## Test Driven Development (TDD)
We practice TDD as much as possible. We write extensive unit tests and acceptance tests to ensure the integrity of each feature. In some situations, we write code first and write tests afterwards. But, usually we write the tests first. And, whenever we change code, we always write tests to ensure we are making the correct modifications.

## Hosting
We host static sites and ember apps with [Divshot](http://divshot.com) and Ruby and Rails apps with [Heroku](http://heroku.com). We are not sysadmins, and find our time is better spent making applications awesome rather than configuring servers. 

## Browser Support
We design and develop for modern browsers. We don’t support IE versions lower than 9. If users visit your app from an old browser, they will see a message that asks them to upgrade to a newer one.

## Monitoring
It’s important to track your application’s performance metrics. We use the metrics feature of the [Heroku dashboard](https://dashboard-next.heroku.com) to look at web response times, CPU, and memory usage. We use [Skylight](https://www.skylight.io) to detect and improve slow actions and queries.

## Bug Tracking
We recommend Bugsnag or Honeybadger to track bugs. We find Bugsnag works best for environments with different types of codebases or separate projects. Honeybadger works best for Rails environments. Other services will probably work fine too. The important thing is that there is a system in place.

---