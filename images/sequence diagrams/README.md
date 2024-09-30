
Copy the below sections to the https://sequencediagram.org/ to render the iamges

title Resume Submission

Candidate UI->ResumeService:Uploads Resume
ResumeService->BlobStorage:Stores Resume
ResumeService<--BlobStorage: ok
ResumeService->]:ResumeEvent 
Candidate UI<--ResumeService:ok


title Job Submission

Employee UI->JobService:Uploads Job Spec
JobService->DB:Stores Job
JobService<--DB: ok
JobService->]:JobEvent
Employee UI<--JobService:ok


title Job Matching

Employee UI->JobService:Get matches
JobService->JobMatchesStorage:Get job to employee matches
JobService<--JobMatchesStorage:return jobId to list of candidates
JobService->CandidateService:Get candidates information
JobService<--CandidateService:return list of candidate information
JobService->ResumeService:Get SMART story for candidate
JobService<--ResumeService:return SMART story for each candidate
JobService->JobService:Filter candidate without SMART story
Employee UI<--JobService:returns matches


title CV Unlock 

Employee UI->JobService:Unlock CV
Employee UI<--JobService:Redirect to payment page
Employee UI->PaymentService:Make Payment
Employee UI<--PaymentService:ok
Employee UI->ResumeService:fetch candidate resume
Employee UI<--ResumeService: return downloadable resume link

