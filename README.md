# CodeMentor_Backgroundjobsystem
Learning Go and other Web frame works
Specs:
The background job system is a common component in the modern workflow. It can run jobs in an async fashion, which reduces the latency for clients. Some common examples include sending an email, scraping webpage, and producing a worksheet. In this project, you'll build a dummy background system
Pre-Reqs & Assumptions:
Client:
     Push job to the queue.
Server:
Pull jobs from the queue and execute them.
Allow the background system to run more than one job at the same time. You'll also need a concurrency limit to avoiding too many jobs at the same time.
Retry the job when the job fails. Each job should have a retry limit.
Actual Scenario:
1.Sending an Event to a middleware when an Account is created in the system
2.so consumers can subscribe to the latest information of the Account
Out-of-Scope:
1.Creation of Account
In-Scope
1.A job is Created in the background to be processed with a defined parameters
    a) based on  the scenario: Account Creation --> Retry 5 times before marking the job as failed
2.Once the Job has been created, Back end servers process the Job
3.
   a)In the Job, each server makes a call to the end-point and marks it as complete
   b)if it fails acheive rerty as defined, once all re-tries are done mark the job as failed
   c) send an email alert to the application admin
Technical Details of the req:
1.Creation of Job with Retry attempts as '5'
2.Universal Application Admin email address as 'dummy_email@gmail.com'
3.System is loadbalanced in assigning the jobs to a correct server
4.Single Client & Single Server(Job monitor)
5.Record deadlock has to be handled
6.Data Base: NoSQL
7.Programming language: Go
8.Webframe work:TBD
9.End-Point is dummy/self and always responds success until an error scenario is tested

