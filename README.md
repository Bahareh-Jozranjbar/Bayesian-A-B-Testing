# Bayesian A/B Testing for UX Research  

## Why Bayesian A/B Testing?  
Most UX research relies on traditional A/B testing, where we wait for large sample sizes before making decisions. But what if we could **update our insights dynamically**, making decisions faster and with fewer users?  

This script demonstrates how **Bayesian inference** helps us:  
- Identify the better-performing UI **faster**  
- Avoid waiting for statistical significance in **classical A/B tests**  
- Make **data-driven UX decisions** with real-time updates  

Instead of just collecting data, we use **Bayesian models** to **predict success rates**, allowing for a smarter and more adaptive approach to UX research.  

---

## How It Works  
This script simulates **500 users** interacting with two different UI designs:  

- **UI A has a 55% success rate** (e.g., users completing a task successfully).  
- **UI B has a 45% success rate** (slightly worse performance).  
- We use **Bayesian inference** to estimate the probability that **UI A is better than UI B**.  

We assume a **Beta distribution** for modeling uncertainty and update our beliefs as we collect more data. The result? A **posterior distribution** that lets us dynamically determine which UI is likely better.  

---

## Installation & Requirements  
This script requires **R** and the following libraries:  

```r
install.packages("ggplot2")
install.packages("dplyr")
```

Once installed, you’re ready to run the script!

## Understanding the Results
### What the Plot Shows
The posterior distributions in the plot represent our updated beliefs about the success rates of each UI:

UI A (blue) and UI B (orange) show the estimated task completion rates.
Dashed lines represent the true success rates (UI A = 55%, UI B = 45%).
The title shows the probability that UI A is better than UI B, based on Bayesian inference.

## Key Takeaways:
- If UI A’s curve is consistently higher than UI B’s, it’s the better choice.
- The probability of UI A being better is calculated dynamically.
- We don’t need huge sample sizes to make a confident decision.

