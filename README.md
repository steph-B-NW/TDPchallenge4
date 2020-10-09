# TDPchallenge4

## Week 4 Challenge

### Task
- **Write a playbook that installs Docker onto the local machine.

##Stretch Goals

- **Create a Docker role.
- **Add a role that will deploy an Nginx container.


## Submission
You should create a Git repository that will contain any playbooks you create.
You are also expected to make a README.md file and to fill this README with information of this challenge. It should contain the following headers.

### What was the challenge?

Rather simply, create a playbook that will manually download and install docker, avoiding the pitfalls of using the curl command that will throw up errors and possibly corrupt your installation. importantly, this will work on multiple machines as it will install the necessary dependencies.

### How I expected the challenge to go.

with the main line of the task being so short, I was ready for some unexpected pitfalls. I was hoping to take a shot at the stretch goals this time.

## What went well?

this is easier to explain once I talk about what didn't go well. Essentially, once I understood my angle of attack better, rather smoothly. I ended up googling the exact syntax which gave me a very solid framework to work from, and it only required a few bugfixes and indentation correction to create a fully functioning build.

## What didn't go as planned?

at first, I was working under the assumption that we would need to create and run a bash script that would be executed within an ansible playbook. I built a bash script that would run the curl command, and the instructed ansible to execute it. this worked with very limited success, and I sought some advice as to the angle I would need to take to create better functionality. I knew I had missed something regarding docker installation, and finally found the advice we had been given earlier regarding manual docker installs. I used this and made sure to lookup the necessary commands that we had not learnt previously, and used them to construct a new ansible script that would use apt to manually request, pull and run the necessary requirements and commands to execute the docker installation, while taking into account the possibility of previous docker installs to prevent corruption.

## Possible improvements for future challenges.

assessing my angle of attack on an issue is important. I didn't fail fast enough.
