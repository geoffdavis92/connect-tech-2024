# Removing Repetition By Building Your Own Automation Framework
*Cameron Presley*

* About
  * blog.thesoftwarementor.com
  * bsky: thesoftwarementor.com
  * blog.thesoftwarementor.com/training
  * Lean Techniques

https://docs.google.com/presentation/d/1bk8Z-jrLIO0zcvuHhe5bAjTK_1I4edZW_LN16SagTuw/mobilepresent?slide=id.g2cd739575a8_0_11

* "Who's on call?"
  * Bystander effect
  * Three Virtues of a Developer - Larry Wall
* Demo
  * PagerDuty + Slack
  * Languages 
    * Typescript
    * Node.js/Deno?
    * Deno
      * first class TypeScript support
      * Good docs
      * Permission scheme
      * Best practice support OOtB
* How to schedule?
  * Task/Cron job? Maybe
  * CI
    * ex GitHub Actions
* Deno
  * init, run, task, test commands OOtB
* GH Action
  * schedule, workflow_dispatch triggers
  * Steps
  * Once in repo, action is running
* PagerDuty Domain Terms 
  * App -> the thing
  * Escalation Policy -> how/when to notify 
  * Sechedule -> who to notify
* Deno permission scheme
  * Requests access to filesystem
  * Ability to fine-tune exposure of which ENV variables
  * `--use-env`/`--env-file`
* Update CI with (variable) secrets
* Webhook
  * Enable in Slack
  * Call webhook from CI script
* Setting up mentions
  * Look up Slack users by email
* How to keep docs up to date?
  * Clone repo with Deno's `command` functionality
  * Find files, parse
  * Get last review date, send info if last reviewed date is undefined or older than 3 months
* Matching up team members for coffee chats
  * Pull org members
  * Fisher-Yates algo for shuffling
  * Post to Slack