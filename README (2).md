# Position Qualification Expert System

Rule-based expert system that determines which positions an applicant qualifies for and explains why they don't qualify for the others.

**Run it:** https://YOUR-USERNAME.github.io/expert-system/

## How it works
- **Input:** single form. Degree and field are validated text (e.g. "BS" is rejected; enter "Bachelors"). Years accept digits only. Yes/no questions use radio buttons.
- **Inference engine:** forward chaining. Derivation rules first establish `csDegree`, `bachelorCS`, `mastersCS`; position rules then evaluate required skills.
- **Output:** qualified positions, unqualified positions with the failed conditions, desired skills (informational), and an inference trace.

## Assumptions
1. A higher CS degree satisfies a lower one (Masters in CS counts as Bachelor in CS).
2. "2 years data architecture and data development" requires 2+ years in each.
3. "Experience in Agile projects" means more than 0 years.

## Source
All logic is in `index.html` (HTML/CSS/JavaScript, no dependencies).
