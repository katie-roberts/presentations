## Where are the slides?

The slides have a large amout of animation in them.  They can be found at https://drive.google.com/file/d/1E9utOD6JhJvWT00lmLA3luGM79xIjN9R/view

### other tools used in workshop
funretro.github.io/distributed  - used to gather questions for the client

## Client Information

### The Brief

You have been approached by a company who provide an application which is used by auction houses to showcase their catalogues.

Current application as presented by the client to the development team.

Requirement is to create a similar app but one with a social element to the page to allow users to leave feedback on the items on auction to try to create a "buzz" around the auction.  They also want to be able to capture their users data so that they can contact them with other auctions that will be of interest to them.

Limited time frame - Big event - Auctioning off something really importand that (work must be completed in the next 3 months) - marketing already been booked in 

Expect an increase in users as a result of this change in functionality.

![Client Described current architecture](https://github.com/katie-roberts/presentations/blob/master/tamingUnicornsWithTechnology/architectures/clientDescribed.png)

### What the client forgot to mention

* Database has not been updated in a long while - old but functional mySQL
* API running on a server 
* server is on physical machine in the company
* Server is running on old version of Windows
* There is a secret config file 
* There are unknown dependancies that also use the API which is why it is not an easy thing to alter the API 
* Database is insecure - would not be suitable for storing user data
* Evernything managed on different deployments
* not all deployment processes are documented or straight forward
* DBA has left the company with no documentation behind  which is why there is another database strapped on for the estimation calculator
* Applicaiton code written by one developer - who managed to complete the code in under a month - no one has been able to really understand what was written since
* No documentation on the API - other developers have looked upon the code and cried
* No documentation on the database
* No access to the Admin system
* Current App was built by a "Rock Star" programmer
* it is only 1 year old
* images for the site are stored in a cloud account (S3 buckets)

![Actual Architecture (incomplete)](https://github.com/katie-roberts/presentations/blob/master/tamingUnicornsWithTechnology/architectures/realArchitecture.png)

Need to know how to get true requirements out of the client - and make them understand what is being asked for.

### suggested solutions

Could the sign in be done via partner system - eg Google?
Does the audience really want to leave feedback on items on sale? Could this be stars rather than words?  (less requirement for moderation)


![Suggested solution - starting to implemet the strangler pattern](https://github.com/katie-roberts/presentations/blob/master/tamingUnicornsWithTechnology/architectures/suggested%20solution.png)