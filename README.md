# UBS-Python-Poetry-CI-CD-Documentation

## Introduction

When we think of setting up a CI/CD framework around an application/project, often within the first few minutes you come across mental roadblocks that seem insurmountable:sweat_smile:. The task gets complex pretty fast when you start thinking of the possible solutions for setting up continuous integration for builds, setting up a versioning convention, pushing the builds to the appropriate artifact registries, pulling those artifacts from the registries and finally deploying them to complete the continuous deployment. It involves taking into consideration a lot of factors and then designing a solution with the tools at your disposal within the organization's guidelines.

Some of the difficult decisions that one might need to take very early on is selecting a good build tool and choosing a convenient artifact registry. This is usually followed up with setting up an authentication mechanism in the pipeline, selecting a branching strategy, designing automations for developer actions, and multiple other items that can be very difficult to think ahead in time for the uninitiated. These tasks become more difficult when you are in a constrained environment within your organization's infrastructure where your choices get limited to the organization approved tooling and processes.

We came across this kind of situation when we worked on Neuron which has a whole framework of services written in Python. With virtually no standards for setting up pipelines for Python builds within the organization, and fixed tooling for continuous integration (our beloved DevCloud Gitlab instance) and continuous deployment (Nexus and UBS Deploy), we had a challenge on our hands. The challenge was to create a CI/CD setup for Python builds that conforms with the organization's standards and guidelines. Continue reading this article to see how the mission was accomplished!  

