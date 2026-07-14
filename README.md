# minor_project3
RedFlag is a pure-SQL fraud detection engine built on a simulated six-month transaction history (200,000 records) from PayFast, a fictional Indian payment aggregator handling UPI, card, netbanking, and wallet payments across 20+ cities. Using only MySQL — no Python, no machine learning — the project identifies 12 distinct fraud patterns hidden in the data, ranging from basic velocity and round-amount clustering to advanced mule-account detection and window-function-based anomaly checks like geographic impossibility and velocity spikes, mirroring the day-to-day analytics work done by fraud teams at Indian fintechs like Razorpay, Cred, and PhonePe.
Patterns detected:

Velocity Fraud — 30+ transactions by one user in a single day

Round-Amount Clustering — repeated exact round-number transactions signaling money laundering

Card Testing — 30+ sub-₹10 transactions in one day

Failed-Then-Succeeded — repeated failed attempts followed by a matching success (card cracking)

Odd-Hour Concentration — 80%+ of activity between 2–5 AM

Mule Accounts — large credits followed by fast, matching debits

Refund Abuse — refund ratio above 40% of total transactions

Merchant Collusion — top 5 users driving 60%+ of a merchant's volume

Just-Under-Threshold (Structuring) — repeated transactions at ₹9,999 to dodge KYC checks

Dormant-Then-Active — 90+ day inactivity followed by a sudden burst of activity

Velocity Spike — monthly transaction count spiking to 5x+ the user's average

Geographic Impossibility — transactions in two different cities within 60 minutes
