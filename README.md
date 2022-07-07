# DevOps coding exercise

This is a take-home programming assignment as part of the the interview
process. This consists of a coding problem and a two-part DevOps problem.

This whole problem is intended to take 8-16 hours, and we typically encourage this to be
done over the weekend. Please direct any questions to your contact.

## Coding Problem:

As a DevOps engineer, you maintain the telemetry of a fleet of crypto nodes. Recently one
of these nodes had a significant clock drift, and we wish to monitor for that clock drift
to understand the overall health of the network.

This network is not something you directly control, either, so you cannot impose a solution
like NTP. We only seek to understand the state of things.

You are tasked with writing a simple clock drift to report the difference in seconds
between the current time on the system and the time reported in some other reliable system.
You are left to decide what that reliable system should be. Outbound network requests to the
internet are allowed, but inbound ones are not.

So for example if the local clock reports:

`Thu, 07 Jul 2022 15:21:18 GM`

And the reliable system reports:

`Thu, 07 Jul 2022 15:21:22 GM`

Your script should print `-4` to stdout and exit. This script will be run by a monitoring
solution periodically and results will be collected into a time series database, so it is very 
important that only an integer value is returned in stdout.

Basically, implement this file: [time-drift.sh](https://github.com/dalvizu/devops-coding-exercise-bash/blob/master/time-drift.sh)

Use any executable or package that you think is necessary.

Finally, write a brief design document [design.md](https://github.com/dalvizu/devops-coding-exercise-bash/blob/master/design.md)
outlining your approach, how you decided on it, and any limitations or future concerns.

The purpose of this is to give you a chance to do some of the work you'd be doing on the job, how you
would approach automating a problem, and how you'd communicate your ideas to your team to solicit feedback
and share knowledge.

Questions are encouraged ask them to your contact. You'll be asked to present your
solution to an interview panel of engineers and argue for any decisions you're making, so be prepared
to discuss your solution.

While this is a standard layout and uses standard libraries, feel free to use any modules you feel 
like and structure this any way you like. Be prepared to discuss your reasoning in the panel interview.

## DevOps problem

### Docker problem

Containerize your solution in a Docker container.

* create a Dockerfile
* provide instructions for how to build and run it.


### AWS problem

You have been provided an AWS IAM credential and a region to use in AWS. Please do not leave this region,
as we need clean up resources after the interview is done.

The problem is to take to take the bash solution and place an archive of it in a public website.
Create this website, registered under a domain name of your choosing, using the most appropriate technology
you can think of.

This website must include a zipped archive of your repo with any instructions you wish to provide about how
to use or evaluate your submission.

Please ensure this is not searchable by a search engine.

Note your website is not required to run any code or have any sort of API. We just want to
see how you work with AWS, how you'd build a website with AWS, and how you'd hand off a completed
project for others to read and use.

Fancy HTML or CSS is not expected, required, or used to evaluate your submission. It can be as ugly
as you like.

However, an infrastructure as code solution IS required, using a technology of your choice.

**NOTE** You will not be able to create or modify any IAM resources in this account due to security
limitations. Your contact will be able to make any necessary roles, policies, etc.. that you require,
provided your reasoning.

## Required Tools

* git
* python3
* pipenv
* docker

## Submitting:

To submit your answer, create a private repository and email that and any instructions for your final submission.

We want to re-use this test on future interviews, so please:

  * Do not make a pull request - these are public and we can't delete them.
  * Do not place your solution in a public git repository 
  * Do not place anywhere else discoverable by a search engine

