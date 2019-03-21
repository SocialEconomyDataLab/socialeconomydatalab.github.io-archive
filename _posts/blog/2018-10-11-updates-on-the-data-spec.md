---
layout:  post
title:  Updates on our data templates
date:  2018-10-11 12:00:00 +0100
category: blog
author:  Tim Davies

excerpt: 
---

**One of the key ideas behind social investment is that one source of funding can unlock others.** Whilst investment can be about taking a risk on new ideas or ways of delivering social impact, projects often seek to distribute risk by combining funding from different sources: accessing capital through a mix of community share offers, loans and grants. 

Getting a clear picture of how this finance interacts, and how it connects with social impact can be challenging. Which is why we've been working to develop a flexible data model that can bring together information on all aspects of a social investment deal. This week we've released the beta version of the model, along with detailed technical documentation and an example data template. 

We've also been piloting the data specification with the Community Shares Unit and Key Fund, and working on prototype dashboard tools to analyse collected data. 

Below you can find out more about the spec, and where we are up to. 

### What is it? 

**A data template...**

The simplest way to think of the SEDL Data Specification is as a **shared data template for social investors**. 

<img src="(https://github.com/SocialEconomyDataLab/socialeconomydatalab.github.io/blob/master/img/blog/template-gif.gif)" width="1000" alt="Animation of the template"/>

If you [look at our documentation, you will find a spreadsheet version of this template](http://spec.socialeconomydatalab.org/en/latest/getting_started/datatemplate/), which is pre-configured with columns for describing social investment deals, the projects they relate to, the assets they invest in, and the different components that make them up, including grants, loans and equity. 

Each column has a definition describing the data it should contain, and many have validation rules to help you enter clear values (e.g. dates, equity amounts and so-on). 

You can use this template to collect, exchange and publish data on social investment deals and projects: and to carry out your own local analysis of your data. 

It takes all the work out of designing your own databases and data collection. 

**...backed by a flexible data model.**

However, if you've already looked at the template - you might be thinking that it's all a bit overwhelming. The 'default' template contains over 220 columns!

And when you enter data, you might quickly hit up against problems where a deal contains multiple grants and loans, yet the template only has columns for one. 

With a normal spreadsheet, if you start removing and moving columns about, then it's going to get tricky to compare your data with someone elses' - as you will have different data structures.

Fortunately, the SEDL Data Specification is backed by a detailed [JSON data schema](http://spec.socialeconomydatalab.org/en/latest/schema_reference/) and a clever set of conversion tools that mean:

* **You can customise the template**, removing columns you don't need;
* **You can repeat rows when a deal involves more than one of key components** such as projects, loans, grants, or equity investments. All you need to include on the additional row is a deal identifier.
* **Data from different template can be 'normalised' into a common structured data model** using [flatten-tool](https://flatten-tool.readthedocs.io/en/latest/)
* **Systems that already store structured data can output it straight away in JSON format** cutting out the need for the spreadsheet in the middle. 

This lays the ground work for integrating data from many different sources. 


### Why a data specification?

Social investment data is collected and stored in many different systems. It might be captured in an investors Salesforce system, or stored in spreadsheets. Or it may be scattered across documents and e-mails. When we started looking at social investment data last year, we found that existing datasets contained a lot of ambiguity that made interpreting the information difficult. It was hard to identify clearly which organisations were involved in a deal, and whether amounts were estimated or confirmed. This all affects analysis, and the kinds of research and intelligence that can be taken from the data. 

The SEDL Data Specification:

* describes how to **bring data together in a common structure and format** so that information can be easily exchanged;

* provides **definitions** of data fields, so that information from different social investors can be combined and compared. 

* gives guidance and **data quality rules** (schema validation) so that data is ready for analysis. 

Social investment is also a diverse field, and so we've made sure the SEDL Data Specification is also flexible and extensible. It covers common data that social investors and researchers may want to share, but also allows data providers and users to choose which elements are relevant to them. 


*(Note: We don't yet call this a 'standard' (unlike, say, the [360 Giving Data Standard](http://standard.threesixtygiving.org/), because at present it doesn't have an established governance model to make decisions over changes to the standard, nor is there currently any initiative to assess published data against the specification.)*


### How was it developed?

In late 2017, we worked with [Power to Change](https://www.powertochange.org.uk/) to look at building data dashboards with key facts on their programmes. With support from Power to Change and [the Connect Fund](https://www.barrowcadbury.org.uk/what-we-do/the-connect-fund/) we started to explore [user needs](http://spec.socialeconomydatalab.org/en/latest/getting_started/use_cases/) for a common data specification that would make it easier to analyse data across different social investment programmes.

Over 2018, we've worked with Key Fund and Community Shares Unit, who have been transcribing historical deal data from a range of systems into spreadsheet templates. Through a number of iterations we've put together the data schema and templates. 

By working in parallel on a prototype data dashboard, we've been able to check that the data model is 'analysis ready'. 

### How can you use it?

Between now and January 2019 we'll be putting the finishing touches to a re-usable dashboard for working with data entered into the SEDL template. However, as the slide deck below describes, you can start using the [data template](http://spec.socialeconomydatalab.org/en/latest/getting_started/datatemplate/) and [specification reference](http://spec.socialeconomydatalab.org/en/latest/schema_reference/) now to design your own data collection and publication on social investment deals. 

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vQupCixEPyBHfED0ZZq-0fbix-EbdQR_3BIFF7rGEz41AXJcr2zPjvd_opHxpQ_sPWC7htm8Nap6Oum/embed?start=true&loop=false&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

If you've got feedback on how the template can be improved, you can [record an issue in the project's issue tracker](https://github.com/SocialEconomyDataLab/spec/issues).
