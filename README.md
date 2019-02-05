# Putting It All Together Group Project

**Table of Contents**

- [Introduction](#introduction)
- [Research Topic](#esearch-topic-mens-attitudes-toward-womens-equality-by-birth-cohort)
- [Technical Details](#technical-details)
- [Assignment 1: Getting Used to Git and Markdown](#assignment-1-getting-used-to-git-and-markdown)
- [Assignment 2: Introduction and Data](#assignment-2-introduction-and-data)
- [Assignment 3: Results](#assignment-3-results)
- [Assignment 4 Full Report](#assignment-4-full-report)

# Introduction

Throughout the remainder of the term, we will be working in groups to build up an analysis of a specific research question, detailed below. You will complete several Putting It All Together assignments that asks you to analyze the dataset using the specific tools you have learned. For each assignment, you will report your results in a brief report. The goal of this set of assignments is to prepare you for the solo research project that you will conduct at the end of the term, in which you will put all of these components together to answer a different research question.

You are free to organize your group as you like, but I recommend that you nominate one person to be the organizational lead for each assignment. This person will be responsible for handling conflicts, knitting final results, and communicating completion to me. You can rotate this responsibility among group members if you like.

## Research Topic: Hard times in childhood and adolescent deliquency

We will use data from the National Longitudinal Survey of Youth 1997 (NLSY97) to analyze how experiences of hardship in a person's childhood are related to delinquency and criminal behavior in adolescence. In addition, we will explore how this relationship varies by urban/rural status (urbanicity). A subset of this data with the relevant variables for the analyis can be found in the `input` directory of this repository. A README file in the `input` directory describes the data and the variables in more detail.

## Technical Details

We will be using several technical tools that will help facilitate group work for this project. You may initially find these tools frustrating due to lack of familiarity, but ultimately they should help your group to better work on this project collaboratively and to track each student's contribution to the project. These tools will also make it easier for me to provide assistance to your group.

All of the work for this project will be done using the [git](https://git-scm.com/) version control system and GitHub classroom. You should read the separate instructions on Canvas about how to install git and how to use it through RStudio. You should also sign up for an account on [GitHub](https://github.com). All of the data and documentation for this project is contained within a git repository that you will clone to your own computer. You can then make changes to files in that repository through RStudio and commit and push those changes so that other group members can see the work that you have done.

We will also be using [R Markdown](https://rmarkdown.rstudio.com/) to write the actual reports as pdf documents. You should read in full the instructions for using R Markdown on the Canvas page and be sure to install the necessary packages in order to run R Markdown through RStudio. R Markdown will allow you to create professional quality reports with your tables and figures fully integrated. All of the reports that you need to create for this project already have R Markdown templates for you to follow in order to produce the report.

Finally, you can and should use the GitHub interface to help coordinate activities between team members. In particular, the **issues** tab above can be used for group communication. You can reference specific team members by prefacing their GitHub user name with a `@` (like twitter). This feature can also be used to get my attention by using `@AaronGullickson` to summon me.

## Assignment 1: Getting used to Git and Markdown

This assignment is intended to ensure that you have git and R Markdown properly installed on your system and understand how to use them.

1. Clone the GitHub Classroom repository for this project through the `New Project` interface in RStudio, as described on the git instructions on the Canvas page. This should make a copy of the entire repository on your system and load the project into RStudio. You can always reload the project into RStudio from your file system by double-clicking the `*.Rproj` file in the directory.
2. Open up the `getting_started.Rmd` file from within RStudio. In the first section, Add a paragraph (at least three sentences) to this document describing yourself. When you are done, commit **and push** your changes. Remember that you must push your changes after the commit in order for other group members to get your changes when they pull. You should also run a pull command regularly to see the descriptions that other committee members have made.
3. Run the code chunk in the `getting_started.Rmd` file entitled `setup`. This code will load the GSS data and install any extra libraries that you will need for the analysis.
4. Work with your group to fill in code for the empty code chunk entitled `make_figure`. This code should produce a figure showing the distribution of the key dependendent variable for your anlaysis. What kind of figure you make will depend on what kind of variable you have. Use the `fig.cap` option to properly caption your figure.

Its possible that you may run into conflicts if you and another group member edit the same line in this document. Don't panic! Just refer to the Canvas page instructions on how to resolve a conflict and fix it.

Once you have completed all of these steps, you can use the knit command in RStudio to turn your `getting_started.Rmd` file into a pdf file. Commit and push all changes to GitHub and submit your pdf file to Canvas to complete the assignment.

## Assignment 2: Introduction and Data

In this assignment, we will write an introduction for the report and begin the analysis of the data. You should use Introduction and Data sections of the `full_report.Rmd` file. You will also want to be sure to read the information about the variables and dataset provided in the README file in the `input` directory.

1. Write an introduction. This introduction should include a statement of the research question (in your own words) and a justification for why it is important to know the answer to this research question. Use your sociological imagination for the justification. This should be a single paragraph.
2. Complete the data section of the research paper. The data section should include an overall description of the dataset (in your own words) being used to analyze the data as well as a description of the key variables used in the analysis. These key variables include the dependent (outcome) variable, the independent variable that are our primary explanatory variable and any variables we are considering as contextual variables. You should include figures showing the distribution of each of these key variables as well as text that describes any key features of these distributions.

Please keep the following guidelines in mind for all project reports:

- Use clear, concise and accessible language throughout the report. Your target reader is not me, but rather a smart group of people who have little experience in interpreting statistics. Your job is to explain your results to them.
- Because you will be describing things that are already described from other sources, be sure to not accidentally plagiarize text. Describe everything in your own words.
- Do not refer to variables by their label in R (e.g. "indegree"). Do refer to variables in concrete meaningful ways (e.g. "number of friend nominations")
- Do not provide a narrative of your R script (e.g. "Then, I ran the tapply command to calculate mean differences between A and B "). Do present the results from your analysis in R in a way that someone who didn't know R from a hole in the ground would understand (e.g. "On average, members of A had XX more friend nominations than members of B").
- Do not use a casual tone. Do use a professional tone.

When your report is ready, one team member should knit the report to pdf and commit and ensure that all changes are pushed to GitHub. The pdf should then be uploaded to Canvas to complete the assignment.

## Assignment 3: Results

In this assignment, we will continue the analysis of the data by completing the Results section of the `full_report.Rmd`. We will now begin to explore the relationship between our key independent and dependent variables. You should do the following:

1. Examine ways to graphically show the relationship. Show this figure in your report and describe what it tells you in words.
2. Estimate the bivariate measure of association between your variables and report the results.
3. Develop models that control for other variables in your dataset to see how robust the result is to such a control. You should include at least two models (one with no controls and one with full controls), but you should also consider adding control variables in thematic blocks as this may help illuminate what variables are changing the relationship. Report your results in a regression model table using `texreg` and describe the results in words. You do **not* need to consider an interaction term in these models.

Refer to the instructions for the previous assignment for further expectations about the report. When your report is ready, one team member should knit the report to pdf and commit and ensure that all changes are pushed to GitHub. The pdf should then be uploaded to Canvas to complete the assignment.

## Assignment 4: Full Report

In this assignment, we will complete the analysis of the  data and create a full report. You should take all of the feedback on the prior two exercises and incorporate that feedback into your final report. In addition, your final report should add two additional items:

1. A model with an interaction term between your key independent variable(s) and your contextual variable. You can include this model in your full regression table and explain it in the text.
2. A conclusion section that summarizes the findings as they relate to the original research question and discusses any weaknesses or concerns you might have about the results.

Refer to the instructions for the previous assignment for further expectations about the report. When your report is ready, one team member should knit the report to pdf and commit and ensure that all changes are pushed to GitHub. The pdf should then be uploaded to Canvas to complete the assignment.
