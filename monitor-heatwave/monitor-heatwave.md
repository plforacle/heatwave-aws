# Monitor HeatWave

## Introduction

The MySQL HeatWave console allows you to monitor the overall and per-node utilization of MySQL HeatWave hardware resources such as CPU, memory, and storage. It also provides a detailed breakdown of your resource consumption, such as data dictionary size, buffer pool size, and database connections.

_Estimated Time:_ 10 minutes

### Objectives

In this lab, you will be guided through the following task:

- Monitor the Cluster
- Monitor the Workload
- Monitor the Autopilot Shape Advisor

### Prerequisites

- An Oracle Trial or Paid Cloud Account
- Completed Lab 3

## Task 1: Monitor HeatWave Performance - Cluster

You can monitor HeatWave performance  by executing the following steps:

1. Click on the **Performance Tab** link
2. Click the **Cluster** button
3. Select the **MySQL HeatWave Cluster**

    ![performance  monitor cluster](./images/performace-monitor-cluster.png "performance  monitor -cluster")

## Task 2: Monitor HeatWave Performance - Workload

The Workload tab display the most recent queries that were executed in HeatWave, allowing you to analyze when a query was executed, how long it took, and what the query actually does. Execute the following steps:

1. Click on the **Performance Tab** link
2. Click the **Workload** button
3. Select the **MySQL HeatWave Cluster**

    ![performance  monitor workload](./images/performace-monitor-workload.png "performance  monitor -workload")

## Task 3: Monitor HeatWave Performance - Autopilot Shape Advisor

Autopilot Shape Advisor analyses the buffer pool usage, workload activity, and access patterns, and then assesses the suitability of the current MySQL shape. The advisor collects statistics at varying intervals and creates a prediction every five minutes while it is active. If there is insufficient or no activity in a five-minute interval Autopilot Shape Advisor cannot make a prediction for that interval. Execute the following steps:

1. Click on the **Performance Tab** link
2. Click the **Autopilot Shape Advisor** button
3. Select the **MySQL HeatWave Cluster**

    ![performance  monitor workload](./images/performace-monitor-autopilot.png "performance  monitor -workload")

By making MySQL HeatWave natively available on AWS, you can very easily benefit from the only cloud database service that combines transactions, analytics, and machine learning services into one MySQL database, delivering real-time, secure analytics without the complexity, latency, and cost of ETL duplication—on AWS.
MySQL HeatWave on AWS is optimized for AWS with a superior architecture that delivers higher performance and lower cost, as demonstrated by industry-standard benchmarks.

You may now **proceed to the next lab**

## Learn More

- [MySQL HeatWave on AWS Service Guiden](https://dev.mysql.com/doc/heatwave-aws/en/)

- [MySQL Database Documentation](https://dev.mysql.com/)

## Acknowledgements

- **Author** - Perside Foster, MySQL Solution Engineering
- **Contributors** - Mandy Pang, Senior Principal Product Manager, Aijaz Fatima, Product Manager
- **Last Updated By/Date** - Perside Foster, MySQL Solution Engineering, February 2024
