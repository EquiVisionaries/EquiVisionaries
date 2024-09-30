# Sequence Diagrams
This document contains sequence diagrams outlining various processes like resume submission, job submission, job matching, and CV unlock.

## Usage
You can now copy and paste the above sections into the [Sequence Diagram Tool](https://sequencediagram.org/) for rendering!

## 1. Resume Submission

```sequence
title Resume Submission

Candidate UI->ResumeService: Uploads Resume
ResumeService->BlobStorage: Stores Resume
ResumeService<--BlobStorage: ok
ResumeService->]: ResumeEvent
Candidate UI<--ResumeService: ok
```

## 2. Job Submission
```sequence
title Job Submission

Employee UI->JobService: Uploads Job Spec
JobService->DB: Stores Job
JobService<--DB: ok
JobService->]: JobEvent
Employee UI<--JobService: ok
```


## 3. Job Matching
```sequence
title Job Matching

Employee UI->JobService: Get matches
JobService->JobMatchesStorage: Get job to employee matches
JobService<--JobMatchesStorage: return jobId to list of candidates
JobService->CandidateService: Get candidates information
JobService<--CandidateService: return list of candidate information
JobService->ResumeService: Get SMART story for candidate
JobService<--ResumeService: return SMART story for each candidate
JobService->JobService: Filter candidates without SMART story
Employee UI<--JobService: returns matches
```

## 4. CV Unlocking
```sequence
title CV Unlock

Employee UI->JobService: Unlock CV
Employee UI<--JobService: Redirect to payment page
Employee UI->PaymentService: Make Payment
Employee UI<--PaymentService: ok
Employee UI->ResumeService: fetch candidate resume
Employee UI<--ResumeService: return downloadable resume link
```


