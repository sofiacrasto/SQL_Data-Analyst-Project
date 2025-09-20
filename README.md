# SQL Data Analyst Project: Fraud Detection with PaySim

Overview

This project applies advanced SQL techniques to the PaySim Synthetic Financial Transactions Dataset【1}, simulating mobile money transfers to uncover fraudulent behavior. It demonstrates how SQL can be used for pattern detection, risk scoring, and temporal analysis—all essential for real-world fraud prevention systems.

📦 Dataset Source
- Name: PaySim Synthetic Financial Transactions
- Source: Kaggle Dataset by E.A. Laxi
- Description: Simulated mobile money transactions based on real-world behavior, including fields like transaction type, amount, origin/destination accounts, and fraud flags

🔍 Key Features
- Recursive Fraud Chain Detection
Tracks how fraudulent transfers cascade across accounts over time.
- Rolling Fraud Analysis
Uses window functions to detect repeat fraud within a 5-step window.
- Multi-CTE Suspicious Transaction Filter
Flags transactions based on large amounts, unchanged balances, and system-generated fraud alerts.
- Zero Balance Detection
Identifies transactions where destination accounts had zero balance before or after the transfer.
- Boolean Fraud Scoring
Assigns a fraud score based on multiple suspicious signals—perfect for dashboards or ML features.

🧪 SQL Techniques Used
- Recursive CTEs
- Window Functions (SUM OVER, ROWS BETWEEN)
- Multi-CTE Joins
- Conditional Scoring Logic
- Temporal Filtering
- Boolean Risk Labeling

  🚀 Getting Started
- Create and use the database:
CREATE DATABASE bank;
USE bank;
- Import the PaySim dataset into a table named transactions.
- Run the SQL scripts provided to explore fraud patterns and scoring logic.

📁 Files Included
- fraud_chain.sql – Recursive laundering pattern detection
- rolling_fraud.sql – Repeat fraud analysis
- multi_cte_fraud.sql – Multi-condition fraud filter
- zero_balance_check.sql – Dormant destination account detection
- fraud_score.sql – Boolean scoring logic for suspicious transactions
- README.md – Project documentation

📈 Use Cases
- Fraud detection dashboards
- Feature engineering for machine learning
- Compliance and audit reporting
- Behavioral pattern analysis in financial system
