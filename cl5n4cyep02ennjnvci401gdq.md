# Retrospective with Mubaraq

Hello Chief,

You are welcome

No long thing

I just want to discuss some technical things I face as a developer. You'll read some things are wonder how I'm that stupid, just remember we are not here to debate that OK. 

I am currently working a software that is partly e-commerce and fintech and here are some lessons learnt

## Plan For Failure 
When rolling out new features or database migrations, plan for failure.
Write a script or have a way to rollback the changes to the database models or the newly deployed features. When your boss and his boss are on your neck to fix the mess, you'd get sloppier and take longer to correct the problem, if you don't end up making it worse. I deployed some changes that broke the app. Thank God a simple git reset rolled back the nonsense I deployed.

## Gradual change
Don't deploy 10 features, 1 million lines of code at once. No matter how good you are, bug go dey. Say you went ahead and deployed your gigantic updates all at once, now monitoring is failing, software is now slower, some parts just don't work!. Where do you know to start from when customers are complaining bitterly and the product owner is highly worried and. Do you rollback 1 million changes (some of which are important to the business) or trace the bugs and start writing patches under duress or leave everything to God?.It happened to me and I no like am, couldn't do anything but keep writing patches and tracing why some certain things are slower and why monitoring stopped working as it should. If its small changes at a time, rollback is easier and you know where exactly to look at.

## Tooling Automation
There's actually so much work to do. So automate any process that's a pattern. Installing packages, updating, tests, deployment. So it was nice having some DevOps skills. Built some CI/CD pipeline to take off some effort that would be spent doing same thing over and over again.

## Measure, Monitor and Alert
Monitoring is basically about keeping a trace on different parts of a software. So, in this project, at this moment, nothing huge is needed yet. I am able to get away with logging at their part of the software. For example, if you make a trade, I log it wether it is successfull or not, with the trade information, when your trade is approved or declined, when you initiate a withdrawal, whats the state of your wallet - before and after, etc. Because I also had a long back and forth with my partner in the course of this project about the speed of some certain process, I had to write a middleware to log every request and time taken, that way I was able to know if some processes are slow because of the backend or not, which processes are slow etc.

Alerting is the responsive component of a monitoring system that performs actions based on changes in metric values. Some metrics were being monitored and alerts are sent to notify the developers and product owner. Some of these alerts are CPU, Memory, Disk space, bug, failures.

One major thing I had to do was on backward compatibility. But I want to get back to work now. So, I might discuss that later.

So, Bye.

See you when next I decide to write.