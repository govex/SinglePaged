---
title: Part 2 - Manage Algorithmic Risk
markdown: kramdown
---

<style>
/* these .colorX values are used to put coloring into the risk matrices */
 .color1 {background-color: #00B050; color: white}   /* low - darker green */
 .color2 {background-color: #92D050; color: white}   /* kinda low - lighter green */
 .color3 {background-color: #FFC000; color: white}   /* medium - yellowy-orange */
 .color4 {background-color: #ED7D31; color: white}   /* medium - orangy-red */
 .color5 {background-color: #FF0000; color: white}   /* kinda high - reddest red */
 .color6 {background-color: #C00000; color: white}   /* high - dark red */
</style>

> ### About the Ethics & Algorithms Toolkit beta release ###
> Welcome to the beta release of our Ethics and Algorithms Toolkit! This toolkit is designed to help governments (and others) use algorithms responsibly. "Beta" means this is a work in progress; expect it to evolve as we learn what works and what does not.
>
> Who is this toolkit for?
> : If you are building or acquiring algorithms in the government sector this toolkit is for you. Though we expect others will find it useful. 
>
> What is the toolkit?
> : The toolkit is really a process. It walks you through a series of questions to help you 1) understand the ethical risks posed by your use of an algorithm and then 2) identify what you can do to minimize those ethical risks.
> 
> What are the parts of the toolkit?
> :  The toolkit comes in several parts:
>    * The introduction to the toolkit (this document)
>    * Part 1: Assess Algorithm Risk
>    * Part 2: Manage Algorithm Risk
>    * Appendices (including a handy worksheet)
>
> Who made this toolkit?
> : The beta release was a collaboration between The Center for Government Excellence (GovEx) at Johns Hopkins, the City and County of San Francisco, Harvard DataSmart, and Data Community DC.
>
> How can I give feedback?
> : Send feedback on our beta release at [https://ethicstoolkit.ai/](https://ethicstoolkit.ai).
>
> How is this toolkit licensed?
> : The content of this toolkit is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/)

# Part 2: Manage Algorithmic Risk #

In the first section of the toolkit, you assessed a variety of risk factors for a set of algorithms you plan to implement. Using the results from that assessment along with this section, you will identify the appropriate mechanisms to help mitigate some of the risks.
Please note:
* Individual mitigations may be useful for multiple risks.
* Not all risks or levels have specific mitigations.
* Some risk subcomponents are included, but others are not.
* Each risk level builds on the previous mitigations. So, if you have a <span class="color6">high</span> risk factor, you should apply the mitigations for <span class="color3">medium</span> and <span class="color1">low</span> as well.

**Instructions:** Select and implement the mitigation mechanism that corresponds to each risk level you selected (return to Ethics & Algorithms Toolkit: Part 1 for your selections from corresponding steps). You may underline, circle, or check mitigations that apply to your scenario. You will find this part of the toolkit split into two pieces: risk-to-mitigation matching (a quick look at strategies) and mitigations in detail (in-depth explanations of those strategies). 

## Risk-to-mitigation matching ##

### Step 1.2.3: Scope Estimate ###
* If you selected <span class="color1">very narrow</span> or <span class="color2">limited/narrow</span>, [engage impacted communities](#mitigation-1-engage-impacted-communities).
* If you selected <span class="color3">substantial</span>, [use public performance monitoring](#mitigation-2-use-public-performance-monitoring).
* If you selected <span class="color6">broad/wide-ranging</span>, create an [Institutional Review Board](#mitigation-3-institutional-review-board) or a [public advisory group](#mitigation-4-public-advisory-group) with decision-making authority for the program.

### Step 1.4: Overall Impact ###
* If you selected <span class="color1">very low</span>, <span class="color2">low</span>, or <span class="color3">moderate</span>, [engage impacted communities](#mitigation-1-engage-impacted-communities).
* If you selected <span class="color4">significant</span>, [use public performance monitoring](#mitigation-2-use-public-performance-monitoring).
* If you selected <span class="color5">high</span> or <span class="color6">extreme</span>, create an [Institutional Review Board](#mitigation-3-institutional-review-board) or a [public advisory group](#mitigation-4-public-advisory-group) with decision-making authority for the program.

### Step 2.3: Appropriate Data Use ###
* If you selected <span class="color1">low</span> or <span class="color3">medium</span>, create a [dialogue with the public](#mitigation-5-public-dialogue) about the new uses of the data as they are applied to algorithms (mitigation 5).
* If you selected <span class="color6">high</span>, [find or create alternate data sources](#mitigation-6-alternate-data-sources) to replace inappropriate ones.

### Step 3.3: Accountability ###
* If you selected <span class="color1">low</span>, use [automated testing tools to periodically evaluate algorithm performance](#migitation-7-automated-periodic-evaluation), ensure there is a [human adjudication mechanism](#mitigation-8-human-adjudication).
* If you selected <span class="color3">medium</span>, [require human intervention before executing each algorithmic decision](#mitigation-9-human-decision-intervention)
* If you selected <span class="color6">high</span>, ensure your [human adjudication mechanism](#mitigation-8-human-adjudication) results feed into [algorithm tuning](#mitigation-8a-algorithm-tuning), ensure the [relevant inputs and machine state(s) are captured in perpetuity for each decision](#mitigation-10-capture-automated-decision-state), and [periodically review human-intervened decisions](#mitigation-11-review-human-intervention-decisions).

### Step 4.2: Third Party ###
* If you selected <span class="color1">low</span> or <span class="color3">medium</span>, formally [transfer liability risk](#mitigation-12-transfer-liability) to the third party(-ies) and [implement independent monitoring](#mitigation-13-independent-monitoring) through an internal mechanism or additional third party.
* If you selected <span class="color6">high</span>, [include contractor incentives for desired outcomes](#mitigation-14-outcome-incentives).

### Step 5.1: Historic Bias ###
* If you selected <span class="color1">low</span> or <span class="color3">medium</span>, tune the algorithm to [systematically minimize bias impact](#mitigation-15-adjust-for-statistical-inaccuracy) and compensate for missing data.
* If you selected <span class="color6">high</span>, do not use the data and find [alternate proxies](#mitigation-6-alternate-data-sources) with [accurate biases](#mitigation-16-improve-data-quality).

### Step 6.1.3: Representativeness and Inaccuracy ###
* If you selected <span class="color6">high</span>, run a [data quality improvement](#mitigation-16-improve-data-quality) project or [find another source of data](#mitigation-6-alternate-data-sources).

### Step 6.2.3 Training Data ###
* If you selected <span class="color6">high</span>, [find a more appropriate source of data](#mitigation-6-alternate-data-sources).

### Step 6.3 Methodology ###
* If you selected <span class="color6">high</span>, recruit algorithmic auditors to [audit for influencing factors](#mitigation-17-audit-influencing-factors), variables, or covariates.

### Step 6.4 Overall Technical Bias ###
* If you selected <span class="color1">low</span> or <span class="color3">medium</span>, [define clear measures of bias](#mitigation-18-define-bias-measures) and monitor your program over time to ensure that it / they does / do not increase.
* If you selected <span class="color6">high</span>, [compare pre-existing bias to predicted bias](#mitigation-19-compare-pre-existing-and-predicted-bias).

### Step 7.0 Overall Risk ###
> **Note:** this risk is not currently calculated in part 1 of the toolkit.

* If you selected <span class="color1">low</span>, [ensure program managers understand and sign off on the risk profile](#mitigation-20-risk-profile-acceptance).
* If you selected <span class="color2">medium</span>, [ensure system users (and impacted individuals) are aware that decisions are being made via automation](#mitigation-21-inform-of-automation) and [apply multiple algorithms to the same decision](#mitigation-22-parallel-algorithms), favoring the decisions which lead to desired outcomes.
* If you selected <span class="color6">high</span>, [delay implementation until risks can be reduced or benefits significantly outweigh the dangers](#mitigation-23-delay-implementation), create an [Institutional Review Board](#mitigation-3-institutional-review-board) or a [public advisory group](#mitigation-4-public-advisory-group) with decision-making authority for the program, and [have researchers periodically evaluate implementation](#mitigation-13-independent-monitoring) and provide reports to the managing authority.




## Mitigations in Detail ##

### Mitigation 1: Engage Impacted Communities ###
Effective community engagement is people-centered, partnerships-driven, and power-aware. Engagement with the community should be social (using existing social networks and connections), technical (skills, tools, and digital spaces), physical (commons), and on equal terms (aware of and accounting for power). An example of engaging impacted communities around open data could look like: the co-production of a policy and open data prioritization, the public creating innovative tools from raw data, and the public then interacting and engaging with data apps and visualization tools.

### Mitigation 2: Use Public Performance Monitoring ###
The purpose of public performance monitoring is to identify areas of good performance and areas where performance can be improved. Performance information should be focused (on the agency’s objectives and services), appropriate (to, and useful for, the stakeholders who are likely to use it), balanced, (giving a picture of what the agency is doing, covering all significant areas of work), robust (in order to withstand organizational changes or individuals leaving), integrated (into the organization), and cost-effective (balancing the benefits of the information against the costs). 

### Mitigation 3: Institutional Review Board ###
An institutional review board (IRB) is a traditional committee established to review and approve applications for research projects. An IRB can also exist in non-academic circles, and its committee members can serve as a necessary step before an algorithm is implemented.

### Mitigation 4: Public Advisory Group ###
Public advisory groups are typically comprised to key stakeholders related to a project as well as representatives of the general public, selected to inform the development of a project.

### Mitigation 5: Public Dialogue ###
Starting a dialogue with the public about new uses of data could be as simple as creating a survey and surveying residents, sending out a weekly or biweekly memo or newsletter to inform residents of new uses, holding town hall meetings in order to discuss the data, publishing open data online, and/or maintaining a public Github. 

### Mitigation 6: Alternate Data Sources ###
Stop the controversy before it starts: Do not start a project with data that has the potential to be harmful. Find or create new data sources by completing a data inventory to locate more appropriate data, researching your topic online to find new data, or collecting new data.

### Mitigation 7: Automated Periodic Evaluation ###
Automating testing tools (i.e. confusion matrices when evaluating classification models) to evaluate an algorithm’s performance can be a way to integrate systematic checks into the lifecycle of an algorithm. If the aforementioned classification model is falsely classifying 70% of cases, the automated testing tool can be programmed to produce “STOP” in red letters.

### Mitigation 8: Human Adjudication ###
A human adjudication mechanism, being a process through which a person can introduce his or her own discernment, can be a great addition to a project involving an algorithm or algorithms. Ensuring that this mechanism can then feed into the tuning of an algorithm can be a great addition to the project.

### Mitigation 8A: Algorithm Tuning ###


### Mitigation 9: Human Decision Intervention ###


### Mitigation 10: Capture Automated Decision State ###


### Mitigation 11: Review Human Intervention Decisions ###
Evaluate human-intervened decisions periodically to control for unintended rater bias.

### Mitigation 12: Transfer Liability ###


### Mitigation 13: Independent Monitoring ###
Shifting the monitoring of an algorithm to an internal or additional third party adds one more level of subjectivity to an algorithm’s methodology. 

### Mitigation 14: Outcome Incentives ###


### Mitigation 15: Adjust For Statistical Inaccuracy ###
Missing data can be a source of statistical inaccuracy in any project. Missing data has the potential to greatly exacerbate harmful bias in the context of algorithms. If you are aware that your algorithm is using data that is largely comprised of missing values, make sure that your algorithm has a way to systematically account for these values. For example: If your dataset is small, you might elect to weight certain demographics within the data in order to more accurately reflect a general population.

### Mitigation 16: Improve Data Quality ###
Running a data management improvement project could consist of: Creating a data governance structure, creating an open data policy, running a new data inventory, constructing an open data portal, committing to a new data publication process or data standards, systematically testing data quality, adhering to a new data retention policy or privacy and security policy, engaging with the community around the data, or hiring new staff and talent. 

### Mitigation 17: Audit Influencing Factors ###
Recruiting algorithmic auditors (statisticians, data analysts, data science professionals, computer scientists, etc.) to audit for the influence of certain factors, variables, or covariates might be very helpful. You might find it helpful to have these auditors routinely return to your algorithm and run a systems check. After rigorously auditing your algorithm, what have they concluded?

### Mitigation 18: Define Bias Measures ###
Being clear and intentful is highly important, regardless of context. In the context of an algorithm, define clear measures of bias and then decidedly monitor your program over time to ensure that it or they does or do not increase.

### Mitigation 19: Compare Pre-existing and Predicted Bias ###

### Mitigation 20: Risk Profile Acceptance ###
Ensure that program managers can understand and are able to sign off on the risk profile that is reflected by your algorithm. Can they explain each risk, and do they understand who or what this risk or these risks might affect?

### Mitigation 21: Inform of Automation ###


### Mitigation 22: Parallel Algorithms ###



### Mitigation 23: Delay Implementation ###

