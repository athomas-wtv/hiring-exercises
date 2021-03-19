# Full Stack Interview Project: Investor Site Enhancements
Candidate: Andre Thomas

## Developer's Notes

First and foremost, I want to thank you for the opportunity to continue in the interview process. I enjoyed the challenge very much.

### Code Readability
In my assessment, there was not much one could do to mess up the readability unless they were trying to. Probably, the area that could have been the source of convolution were the calculating of dollar amounts. There are ways to do these calculations in one or two lines but that would have been unhelpful to other devs who may need to make updates in the future. I broke many of the variables up so that readers can follow the logic.

### Code Extensibility
I added a component called "Message". I did this because a scalable app would utilize many messages for a better UX. Now, as this foo app scales, devs can use this component to add messaging throughout the application.

There are ways to make that component more robust. One could add classes, styling, or even other variables that hide and show certain elements for more effects (i.e. a fontawesome icon).

## Tests
I created a test to check to see if the correct error code came back unauthorized if someone entered in invalid credentials.

### Difficulties
One of the challenges that I faced was the Vue.js learning curve. Before our interview, I have never touched this library but I have come to enjoy it's simplicity. After our interview, I began watching LinkedIn Learning tutorials to wrap my head around it in preparation for this challenge. The time spent served me well--all things considering :)

Another challange was the api calls. I added two comments on the Dashboard component letting you know what I would have done had I gotten it to work. I wanted to make you all aware that  I am familiar with js promises. In my current job, I make http calls all the time (i.e. `$http.get`) from AngularJS to .NET endpoints via promises and manipulate the data I get back. That's what I was looking to do but just couldn't in this short of time. What I would have done with the data I got back is listed in the comments.

### Conclusion
Although, I could only successfully completed one story, I am confident in my ability to finish the last two had I gotten the api calls working. Thank you, again, for your time and I look forward to the next steps if you think my skills warrant further interviewing. Take care!

## User Stories
---
### Login failure isn't handled gracefully
**Context**

**As an** Investor
**I want** to know if I input incorrect credentials
**So that** I can check my input

**Acceptance Criteria**

**Given** I am not logged into the site

**When** I enter invalid credentials (Backend responds with HTTP 401 Not Authorized)

**Then** I should see an error notification that my login attempt was unsuccessful

---
### BUG Unauthenticated users can browse to the dashboard
**Expected Behavior**

Browsing to /dashboard redirects to login

**Actual Behavior**

Browsing to /dashboard renders empty page

**Acceptance Criteria**

**Given** I am not logged into the site

**When** I visit /dashboard

**Then** I should be redirect to login at the site root

---
### Investor Should be able to see Amount of Expected Return

**As an** Investor
**I want** to headline stats about my account
**So that** I can review my investment at a glance

**Acceptance Criteria**

**Given** I am logged into the site

**When** I view the dashboard

**Then** I should see my Initial Investment amount listed in the headline stats

**And** I should see my Investment date listed in the headline stats in human readable format

**Also** I should see my projected value amount listed in the headline stats

**Dev Notes**

Headline value is calculated as:  P (1 + r/n)^(nt), where P is the initial principal balance, r is the interest rate, n is the number of times interest is compounded per time period and t is the number of time periods. e.g.
P = 5000.
r = 5/100 = 0.05 (decimal).
n = 12.
t = 10.

A = 5000 (1 + 0.05 / 12) (12 * 10) = 8235.05.

---
### Investor Should be able to see Amount of Deposit/Withdrawal

**As an** Investor
**I want** to view the amount of transactions
**So that** I can easily track the balance

**Acceptance Criteria**

**Given** I am logged into the site

**When** I view the dashboard

**Then** I should see any account transactions listed

