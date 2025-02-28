Building a Fraud Rule Engine and Refund Denial Engine for Quick-Commerce
Quick-commerce companies, with their rapid order processing and delivery times, face unique challenges in maintaining operational integrity. One significant issue is detecting and preventing fraudulent activities, especially in the realms of refunds and discounts. During my tenure at India’s biggest quick-commerce company, I spearheaded efforts to develop a fraud rule engine and refund denial engine. Here, I will share the methodologies, insights, and outcomes of these projects.

Key Metrics to Monitor
To effectively track fraud and refund activities, we identified several critical metrics:
Refund Percentage of Gross Transaction Value (refund%gtv): Indicates the proportion of gross transaction value attributed to refunds.
Discount Percentage of Gross Transaction Value (discount%gtv): Reflects the share of discounts applied relative to the overall transaction value.
Discounted Orders Percentage: Tracks the ratio of orders placed with discounts.
Refunded Orders Percentage: Highlights the proportion of total orders that were refunded.
These metrics were visualized using a Tableau dashboard. The dashboard incorporated filters such as:
City-level Analysis
Refunded Cohorts: Grouping users based on the number of refunds requested versus their total orders.
User Cohorts: Segmented by the number of orders placed in the last 90 days.
This dashboard allowed us to determine whether high refunds or discounts were prevalent and to analyze the types of users requesting refunds.

Addressing Refund Fraud
Initial Approach: Machine Learning Model
Our initial plan was to build a machine learning model that could predict fraudulent refunds based on a user’s order and refund history. However, this approach faced several challenges:
Real-time Deployment: Ensuring the model’s predictions were available instantly.
Accuracy Concerns: Sole reliance on order history data didn’t yield satisfactory results.
Shift to a Heuristic Model
Given the limitations of machine learning, we pivoted to a heuristic-based model. This approach required extensive research to define initial rules that served as the baseline. New rules were added as emerging fraud patterns were discovered.
Key Insights:
Syndicate Behavior: Refund fraudsters often operate in syndicates, clustering geographically.
Location-Based Rules:
Using latitude and longitude data with a 10-meter accuracy, we identified and mitigated approximately 90% of fraudulent activities.
Regularly refreshed location data to adapt to changes.
Introduced a whitelisting mechanism for genuine users in apartments and densely populated urban areas. This reduced false positives significantly.
Results:
Achieved an accuracy rate of 96% in identifying fraudulent refunds.
Addressed false positives through a support workflow. Genuine users were tagged upon reaching out to support, as fraudsters rarely engage with customer support.
Optimizing Agent Workload
To minimize manual intervention, we categorized rules into:
High Confidence Rules: Set with strict thresholds to ensure 100% accuracy for detecting fraudulent refunds.
Low Confidence Rules: Required manual review by support agents for borderline cases.
This segmentation reduced agent workload while maintaining fraud detection effectiveness.

Broader Learnings and Future Scope
Dynamic Rule Refinement: Continuously monitor and adjust rules to address evolving fraud tactics.
Scalability: The rule engine can be expanded to detect other types of fraud, such as fake orders or unauthorized discounts.
Integration with Analytics: Leverage user behavioral data for deeper insights, potentially incorporating advanced techniques like graph-based anomaly detection.

Conclusion
The fraud rule engine and refund denial engine we built transformed how our organization tackled fraudulent activities. By leveraging a combination of heuristic models, real-time location data, and intelligent workflows, we achieved a significant reduction in fraudulent refunds. This solution not only saved costs but also ensured a better experience for genuine customers.
This project highlights the importance of adaptability and iterative refinement in addressing complex challenges in quick-commerce operations. I look forward to implementing similar innovative solutions in future endeavors.
