# Digital-Payment-Behavior-Segmentation-using-Clustering

1. Problem Statement

A digital payments company operating in the UPI and wallet ecosystem wants to understand how users behave on its platform. Not all users interact with the app in the same way. Some users make many small transactions daily, some make fewer but high-value payments, some are heavily merchant-oriented, some are largely inactive, and some may show unusual or suspicious usage patterns such as high night-time activity, high failure rate, or repeated refund requests. The business currently has rich transaction-level and behavior-level data, but it does not have a predefined target label such as “good user”, “risky user”, or “high-value user”. Because of this, supervised learning is not the right starting point. Instead, the company wants to segment users into natural groups based on their payment behavior so that it can understand its user base more deeply and design more precise operational, engagement, and risk strategies.

The objective of this project is to apply clustering techniques to group users with similar payment patterns. The output of the project should help the company identify meaningful behavioral segments such as high-frequency micro-payment users, premium spenders, merchant-heavy users, low-engagement users, and suspicious or anomalous users. These clusters can then be used to improve customer engagement, feature design, cashback strategies, fraud monitoring, and platform growth decisions.

2. Domain Knowledge

• Digital payment ecosystem: UPI and wallet platforms record not only amounts and counts, but also behavioral signals such as transaction timing, session activity, failures, refunds, merchant usage, and peer transfers.

• Behavior-based segmentation: In this domain, users are better understood through usage behavior rather than only demographics. Two users of the same age or city may behave completely differently in frequency, value, or risk patterns.

• Merchant vs peer payments: Merchant-heavy users typically use the app for shopping, bill payments, food delivery, subscriptions, and in-store payments, while peer-heavy users may use it more for transfers between friends, family, or small business settlements.

• Failure and refund patterns: High failure rates can signal technical friction, poor network conditions, incorrect payment flows, user confusion, or in some cases suspicious patterns. Refund frequency can indicate merchant issues, product quality problems, or abuse behavior.

• Night-time and weekend patterns: Transaction timing matters. Moderate night usage can be normal, but extreme concentration of activity during odd hours may indicate unusual behavior, especially when combined with high failures or refund activity.

• Session behavior: App sessions, open frequency, and session duration provide context around user engagement. Highly active users usually show stronger repeat usage and shorter decision times, while confused or suspicious users may show abnormal patterns.

• Suspicious behavior: Suspicious behavior in a payment system is rarely identified using a single variable. It usually emerges through combinations such as high transaction velocity, elevated failure ratio, high peer transfer concentration, high night usage, and unstable spend patterns.

• Business impact of segmentation: User clusters can support cashback campaigns, merchant partnerships, product personalization, churn prevention, payment UX improvements, and anomaly investigation.

3. Data Dictionary

Column Meaning

user_id:- Unique identifier for each user.

city City:- associated with the user profile.

device_type:- Primary device used for transactions, such as Android or iOS.

kyc_level:- KYC completion status such as Minimum, Full, or Premium.

account_age_months:- Age of the account in months.

account_age_band:- Grouped version of account age for easier business interpretation.

active_days_per_month:- Number of days in a month on which the user is active.

transactions_per_day :- Average number of transactions made per active day.

monthly_transaction_count :- Estimated total number of transactions in a month.

avg_transaction_amount :- Average amount spent or transferred per transaction.

max_transaction_amount :- Maximum single transaction amount observed.

total_monthly_spend :- Estimated total transaction amount for the month.

merchant_txn_ratio :- Proportion of transactions made to merchants.

peer_txn_ratio :- Proportion of transactions made to peer users.

merchant_count_month :- Estimated count of merchant transactions in a month.

peer_count_month Estimated :- count of peer transactions in a month.

failed_transactions :- Number of failed payment attempts.

failed_txn_ratio :- Proportion of failed transactions out of total transactions.

refund_requests :- Number of refund requests raised by the user.

refund_ratio :- Proportion of refund requests relative to total transactions.

night_txn_ratio :- Proportion of transactions happening at night.

weekend_txn_ratio :- Proportion of transactions happening on weekends.

session_count :- Number of app sessions in the month.

app_open_frequency :- Number of times the app is opened in the month.

avg_session_duration_min :- Average time spent per app session in minutes.

avg_gap_between_txn_hours :- Average time gap between transactions in hours.

spend_volatility :- Variation in spending behavior; higher values indicate unstable or fluctuating transaction amounts.

avg_balance_before_txn:- Estimated average account balance before a transaction.

cashback_usage_ratio:- Proportion of usage influenced by cashback or incentive-driven behavior.

suspicious_activity_score :- Composite behavioral score indicating how unusual the payment pattern appears.
