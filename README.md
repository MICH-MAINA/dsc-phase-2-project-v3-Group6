# Box Office Intelligence: Data-Driven Insights for a New Movie Studio

### **Executive Team**


|Team Member                                | Email                               |
| --------------------------------------- | ------------------------------------------------------------------------------------ |
| **Jeremy Onsongo** | jeremy.onsongo@student.moringaschool.com                        |
| **Mary Okello**                          | mary.okello@student.moringaschool.com                                                                |
| **Michelle Ngunya**                     | michelle.ngunya@student.moringaschool.com                                      |
| **Michelle Maina**                      | Smichelle.maina1@student.moringaschool.com                                                   |





## Introduction 

Our company is launching a new movie studio and needs data-driven guidance on what types of films to produce. Inspired by major studios’ success with original content, we analyzed historical box office and ratings data to identify which genres and budgets lead to the strongest financial and audience outcomes.

## Objectives

**Business Questions We Explored**
1. Which genres are currently delivering the highest box office revenue? 
We wanted to pinpoint the most financially promising types of films to help focus our investments.

2. How do production budgets and genre choices interact to impact revenue? 
We needed to understand whether spending more in certain genres produces higher returns.

3. Which genres earn the highest audience ratings and which genres strike the best balance between ratings and revenue? 
We set out to identify the types of films that are not only profitable but also positively received by audiences, ensuring long-term brand value for our studio.

## Describing the Target Audience

| Question                                | Our Answer                                                                           |
| --------------------------------------- | ------------------------------------------------------------------------------------ |
| **Who is receiving this presentation?** | Company leadership & decision-makers for the new movie studio                        |
| **Background**                          | Mostly non-technical                                                                 |
| **Decision impact**                     | Deciding which genres and budgets to greenlight                                      |
| **Attention span**                      | Short want key takeaways quickly                                                   |
| **Goal**                                | Convince leadership that our results guide profitable, well-received film production |


## Narrative Arc

**Problem:** Our new studio doesn’t know what kind of movies to make.

**Approach:** Analyze historical data on budgets, genres, revenue, and ratings.

**Findings:** Budget is the biggest driver of box office, but genre also matters.

**Solution:** Focus on high-performing genres like Animation & Adventure, and use prestige genres strategically for reputation.

## Data Overview

**Sources:** Historical box office data (worldwide gross), production budgets, genres, and IMDb-style vote averages.

**Variables:** 

    - Production_budget 
    - Worldwide_gross 
    - Vote_average 
    - Genres 

## Analytical Approach

**Revenue Model:** OLS regression of worldwide gross on production budget + genre dummies.

**Ratings Model:** OLS regression of average ratings on genre dummies.

**Visualizations:** Top genres by average revenue, top genres by ratings, combined chart of revenue vs. ratings.

## Model Results
### Revenue Model
We used an OLS regression to measure how much of a film’s worldwide revenue can be explained by its budget and genre.

1. R² = 0.608

    - About 61% of the variation in worldwide gross is explained by budget + genre.
    - Business takeaway: we can reasonably predict revenue using these variables, but other factors still matter.

2. Production Budget Coefficient = 3.317 (p < 0.001)

    - Every $1 spent on production yields about $3.32 in worldwide gross on average, controlling for genre.
    - This confirms why major studios invest heavily in tentpole films.

3. Animation Genre Coefficient ≈ +$76M (p ≈ 0.001)

    - After controlling for budget, animated films earn about $76 million more on average.
    - This is the only genre with a statistically significant uplift in revenue once budget is included.

### Ratings Model

1. R² = 0.071
    - Only 7% of the variance in ratings is explained by genre.
    - Business takeaway: audience scores depend on many other factors (script, casting, marketing).

2. Top Positive Genre Effects on Ratings:

    - History (+0.43), War (+0.41), Drama (+0.34), Animation (+0.23) — statistically significant increases on a 10-point scale.

3. Largest Negative Effect: Horror (−0.57) on average, horror movies score more than half a point lower.

Interpretation:

    - “Prestige” genres (History, Drama, War) earn higher ratings but not necessarily higher grosses.
    - Animation stands out as the only genre with both a revenue and rating boost.

## Key Visual Insights

1. Adventure, Animation, Science Fiction lead in average revenue.
![alt text](image-2.png)

2. History, War, Drama lead in average ratings.
![alt text](image-1.png)

3. Animation appears near the top for both revenue and ratings.
4. Horror underperforms on ratings and shows no significant revenue advantage after budget control.

![alt text](image-4.png)

## Recommendations for the Studio

1. Flagship High-Budget Animated or Adventure Films for predictable revenue.
2. Select Prestige History/Drama/War Projects to build critical acclaim and awards reputation.
3. Be Cautious with Horror movies as it has more polarizing ratings and no clear revenue uplift once budget is considered.
4. Allocate production resources carefully; marketing and franchise strategy will further influence success.