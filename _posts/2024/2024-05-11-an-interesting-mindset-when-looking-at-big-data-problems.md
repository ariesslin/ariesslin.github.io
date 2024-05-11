---
title: An interesting mindset when looking at big data problems
author: ariesslin
date: 2024-05-11 01:55:00 +0100
categories: [Blogging]
tags: [Learning Notes]
---

I found this slide by Matei Zaharia on the internet: [Design and Evolution of Data Platforms](https://canvas.stanford.edu/files/7194229/download?download_frd=1&verifier=FURSC3KOxraw9KRiJupUgU77ybCWnbYCeaqjTCjY).

---

It is a presentation used at Stanford University to discuss the history of data platforms, the challenges of data today, and the solutions offered by Databricks.

As Matei Zaharia is the author of Apache Spark and the founder of Databricks, it is very interesting to understand from his point of view how he looks at the big data problem.

Most of the content of the slide can be found in similar materials on the internet if we put in some effort to search. However, one little-repeated narrative caught my attention; I think it is very inspiring, as it can explain the root cause of most failed projects today, especially those built by engineers with "past successful experiences".

The narrative is: most of the core problems are that the amount of data exceeds the limit that humans can review.

I think this is a great mindset to approach most big data problems. When we get some amount of data from certain resources, we should ask ourselves, with today's technology, is there a way to help me summarize this data quickly at an economical cost? If yes, I don't have to reinvent the wheel; I should buy instead of build.

I actually experienced a project in which I was not in a position to decide on the high-level architecture due to roles and other ways of working setup issues, and I struggled to see the client waste time and money (8 months, regularly 8 team members) investing in a bespoke solution that was not easy to scale, had poor performance, and included a lot of manual checks that were error-prone. In the end, the amount of data that just came from the same database was actually easy to be checked and reviewed by just an easy application; there was no need to waste all these resources to build a throw-away solution.

I don't find value in this experience, and I struggled to find the right narrative mindset to help me identify the root cause of why I was unhappy and always felt there was something wrong with that project. Now that I have this new metric -- data amount (not just the volume) vs. human check limitation, I find it helpful to identify the correct business-tech solution for big data problems.

Talking back to the same project experience, the pain point of the client sits in fact that the old product generates a lot of time-series raw data, and it is difficult to extract that data out of the old system, which, in my opinion, should have been the focus point of the project, and that's where a solution of big data platform can shine. Those raw data require a lot of effort to clean and extract value. And even in this case, the bespoke data ingestion part could be challenging and add value, while in other parts the wheel doesn't need to be reinvented; there are already mature solutions (For example I can name cloud storage, dataflow, BigQuery etc).

And that's it for this learning note.

I also want to take this opportunity to say that I might not be suitable to work as a consultant in a hierarchical consulting company as it is slowly going to be. I still feel being a consultant is good, that it can help clients solve their problems, but I would prefer to be in a position where I can find clients who have a strong feeling of ownership and a clear pain point, and as a consultant, we can influence the clients both to buy in or not to buy in. If we feel the client is wasting their money, we just clearly say no. (Yes, that's the old time when my current company was famous for its values).

Well, we will see. If the environment won't change, I will change my environment.
