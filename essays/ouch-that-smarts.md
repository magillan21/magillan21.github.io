---
layout: essay
type: essay
title: "Ouch, that smarts!"
# All dates must be YYYY-MM-DD format!
date: 2025-01-28
published: true
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img width="375px" class="rounded float-start pe-4" src="../img/glitterypopcorn-wizard.png">

## Smart, a guide.
The term “smart” may refer to the adjective used to denote a quick-witted and intelligent individual—or the verb you might use to scathingly signal a stinging and sudden pain; a question posed can lead to either of the two definitions identified. A real smart (adjective) question is relatively simple, as long as the query follows several guidelines: 

* The Enquirer has exhausted the resources available to them (“RTFM” & “STFW”).
* The Enquirer best clean up their grammar. (“I just ate, grandma!” versus “I just ate grandma!”)
* The Enquirer must not faff around—have mercy and be succinct. 
* The Enquirer must be humble yet refrain from grovelling. 
* The Enquirer should discuss their issue’s symptoms—do not diagnose.
* The Enquirer should discuss goals, not steps.
* The Enquirer should avoid listing buzz words such as “URGENT!” or “HELP! HELP! HELP!” (unless, of course, the Enquirer is querying from the International Space Station, then the former does not apply.)
* The Enquirer must not engage in shady private e-mails and follow a transparent and public process.
* The Enquirer must drink their milk and diligently finish their homework. (That’s how Enquirers grow!)
* The Enquirer must be gracious and conclude their query once the solution has been found. (Please find a suitable phrase to express gratitude that falls in-between “Gramercy, goode folke for thine aide. I, the Enquirer, humbly extend mine gratitude for thee, graceful and divinely-favored.” and “thx.”)


## A Smart Venture
Many such examples exist on Stack Overflow, one which will be inspected and its answers examined in order to evaluate the reapings of asking such a smart question. Behold and rejoice: 
```
SSL: CERTIFICATE_VERIFY_FAILED certificate verify failed: unable to get local issuer certificate (_ssl.c:1129)')))

I'm working on scripts to connect to AWS from Win10.
When I try to install a python module or execute a script I get the following error:
[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: unable to get local issuer certificate (_ssl.c:1129)
I've verified that the certificate in the environment path is defined so, besides that, I'm not sure what else to use to troubleshoot the issue.
```
**“SSL: CERTIFICATE_VERIFY_FAILED certificate verify failed: unable to get local issuer certificate (_ssl.c:1129)')))”**
  
Witness the title of this query—a sleek design—how minimalist, how admirable. Next, inspect the actual contents. The first line reads: **“I'm working on scripts to connect to AWS from Win10.”** It is precise in its machinations and denotes the environment the Enquirer is working in; the text is regular plain text mail, which helps its simplicity. The Enquirer, helpfully continues—**"When I try to install a python module or execute a script I get the following error:[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: unable to get local issuer certificate (_ssl.c:1129)"**

Quick and easy to describe the symptoms, and even quicker to describe the goal: **“I've verified that the certificate in the environment path is defined so, besides that, I'm not sure what else to use to troubleshoot the issue.”**

Please notice, not only what the Enquirer is working towards (“troubleshooting”) but also what the Enquirer has previously done to help themselves—this ensures that there are no redundant responses as well as displaying their own agency. But what is the point of such diligence? Behold once more, the foremost answer:
```
Try this in the command line:
pip install pip-system-certs
I've been struggling with the CERTIFICATE_VERIFY_FAILED error as well when using the requests module. I tried installing certifi but that didn't help. The only solution to my problem was to install pip-system-certs. For some reason that allowed requests to access a local certificate.
Also: requests.get(url, verify=False) is not recommended for production environment because you basically turn safety off.
```

Wham-bam-shang-alang! The Enquirer has deemed this the best answer, and has courteously accepted it with a green checkmark. Many huzzahs, and shakes of ale mugs. However, in order to dissect a smart question, one must turn to the dark side and observe a not-so-smart question. Look, here:
