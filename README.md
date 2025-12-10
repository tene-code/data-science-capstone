# data-science-capstone
Capstone project for completion of Data Science minor

# R for Everyone: Data Science for Middle Schoolers

Capstone project for completion of the **Data Science minor** (Fall 2025)  
Pomona College / Claremont Colleges

---

## Project Overview

**R for Everyone** is a four-lesson, interactive micro-curriculum that helps **middle school students (grades 6–8)** build foundational **data literacy** and **ethical reasoning** using R as the engine behind the scenes.

Each lesson is built as a `learnr` tutorial in R and deployed as a **shinyapp**, so teachers and students can access it through a simple web link—no local installation or coding background required.

The curriculum aims to:

- Introduce core ideas in **data, chance, and variability** in an accessible way  
- Give students practice **asking questions, reading graphs, and telling data stories**  
- Embed **ethics prompts** about bias, fairness, and representation directly into math tasks  
- Provide teachers with **plug-and-play lessons** that fit into an existing middle school course

---

## Motivation & Background

Recent work from **Data Science 4 Everyone (DS4E)** and NAEP highlights a worrying trend:

- Between **2019 and 2022**, 8th grade performance on **Data Analysis, Statistics, and Probability** fell significantly on NAEP.  
- Only a small fraction of high school students take a course that looks like **modern data science**, and access is uneven across districts.

At the same time, students live in a world where data drives newsfeeds, recommendations, policing, health, and finance. This project responds to that gap by designing **short, realistic, ethics-aware data lessons** that can slot into a middle school classroom without requiring teachers to become programmers.

---

## Curriculum Structure

The four lessons are aligned with the **GAISE II** statistical problem-solving cycle:

> **Ask → Collect → Analyze → Interpret & Communicate**

Each lesson has a specific role:

1. ### Lesson 1 — Ask a Good Question
   - Distinguish between **opinion questions** and **statistical investigative questions**.  
   - Sort example questions into “can use data to answer” vs. “cannot.”  
   - First ethics prompt: *What happens if you only survey your friends? Who is left out?*

2. ### Lesson 2 — Collect & Visualize Data
   - Work with a small, **simulated classroom survey** on minutes read last night and device used (phone/tablet/laptop/paper).  
   - Explore the dataset in a simple table and **view plots** of minutes read by device.  
   - Discuss typical values, variability, and limitations of such a tiny sample.

3. ### Lesson 3 — Analyze Patterns
   - Reuse the same reading dataset to **compare device groups**.  
   - Interpret a **boxplot** of minutes read by device type.  
   - Practice careful language:  
     > “In this sample, tablet users read more minutes on average than phone users”  
     versus overstrong claims like “Tablets make kids read more.”

4. ### Lesson 4 — Interpret & Communicate
   - Introduce a new, **simulated sleep dataset** (hours of sleep, device in bedroom, sports team, etc.).  
   - Students interpret a **provided graph and summary table** instead of coding from scratch.  
   - Study a **model data story** that combines:
     - a graph  
     - a key number (mean/median)  
     - a clear statement of limits (“in this sample”)  
   - Critique over-claiming blurbs and write their **own short data story**.

Across all lessons, students interact by clicking, choosing answers, and typing short responses—**no prior coding** is assumed.

---

## Design Frameworks

The project is grounded in several existing frameworks and resources:

- **GAISE II (ASA, 2020)**  
  Provides the **Ask → Collect → Analyze → Interpret & Communicate** structure used to organize the four lessons.

- **Data Science 4 Everyone (DS4E)**  
  Supplies national context (NAEP trends, course-taking patterns) and motivates the push for **modern, technology-supported data experiences** in K–12.

- **Chiodo et al. (2023/2025), “Teaching Resources for Embedding Ethics in Mathematics” (arXiv:2310.08467)**  
  Informs the decision to embed **short ethics prompts** directly inside everyday math tasks rather than as a separate unit.

- **youcubed “Big Ideas” in Data & Statistics**  
  Supports the emphasis on **patterns, sense-making, and communication**, especially in Lesson 4’s data storytelling.

---

## Technical Stack

All lessons are built in R and delivered through the following tools:

- [`learnr`](https://rstudio.github.io/learnr/) for interactive tutorials  
- `shiny` / shinyapps.io for deployment as **web-accessible lessons**  
- Simulated toy datasets (reading & sleep) created inside the R code

Key design choices:

- **No real student-level data is used.**  
  All “classroom” datasets are small, simulated tables designed for instructional use.

- **No automatic logging of student responses.**  
  Quizzes and free-response questions run locally in RStudio or in the web app; logging is disabled in the prototype to avoid storing identifiable data.

- **Teacher-controlled storage (optional).**  
  If teachers want to keep student work, they can use their own tools (e.g., Google Forms or an LMS) to collect written reflections or screenshots.

---

## Repository Contents

This repo contains both the **curriculum code** and the **written capstone**. Key items include (names may evolve slightly):

- `Final_Writeup.Rmd` / `Final_Writeup.pdf`  
  Full written thesis / project report (motivation, design, pedagogy, ethics).

- `Project_Draft.Rmd`  
  Earlier draft of the write-up.

- `Lesson1_*.Rmd`, `Lesson2_*.Rmd`, `Lesson3_*.Rmd`, `Lesson4_*.Rmd`  
  Source files for the four `learnr` tutorials.

- `slides/` (if present)  
  Presentation slides for the final capstone talk.

- `README.md`  
  You’re here!

---

## Running the Lessons Locally

You can run the lessons locally in RStudio as follows:

```r
# install packages if needed
install.packages("learnr")
install.packages("shiny")

# from within this repo directory:
rmarkdown::run("Lesson1_Ask_Question.Rmd")   # example name


