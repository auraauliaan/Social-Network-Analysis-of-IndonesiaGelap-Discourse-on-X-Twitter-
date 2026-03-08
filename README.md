# Social Network Analysis of #IndonesiaGelap Discourse on X (Twitter)

This repository contains a research project that analyzes the spread and interaction patterns of the **#IndonesiaGelap** hashtag on the social media platform **X (formerly Twitter)** using the **Social Network Analysis (SNA)** approach.

The study aims to identify the **structure of the social network, key actors, and interaction patterns** that influence the dissemination of information related to the hashtag.

---

# Abstract

Social media has become an important platform for expressing public opinions on social, political, and economic issues. This study analyzes the hashtag **#IndonesiaGelap**, which recently gained significant attention on the X platform.

Using the **Social Network Analysis (SNA)** approach, this research identifies patterns of information dissemination, network structures, and key actors involved in the conversation.

The dataset was collected through **data scraping using Tweet Harvest**, and the network analysis was performed using **Gephi** along with **Python** for additional analysis. The results show that interactions within the **#IndonesiaGelap** discussion tend to be **passive**, where most users interact through likes and reposts rather than direct conversations.

---

# Research Objectives

The objectives of this study include:

* Identifying the **structure of the social network** formed by the hashtag **#IndonesiaGelap**
* Analyzing **interaction patterns** among users on X
* Detecting **key actors** who play important roles in the spread of information
* Evaluating how social media functions as a platform for public opinion expression

---

# Dataset

The dataset was collected by scraping posts containing the hashtag **#IndonesiaGelap** on the X platform using **Tweet Harvest**.

Dataset characteristics:

* Total tweets collected: **3,054 posts**
* Data collection period: **18 – 27 February 2025**

Main attributes in the dataset:

* `username`
* `reply_count`
* `quote_count`
* `retweet_count`
* `favorite_count`

---

# Methodology

This research applies **Social Network Analysis (SNA)** to understand relationships and interactions between users in the network.

## 1. Data Collection

Data was obtained through scraping posts containing the hashtag **#IndonesiaGelap** using Tweet Harvest.

## 2. Data Preprocessing

The preprocessing stage includes:

* Removing duplicate data
* Handling missing values
* Selecting relevant interaction features
* Combining `retweet_count` and `quote_count` into **repost_count**
* Creating a **weight column** to measure interaction strength

Weight calculation:

```
Weight = favorite_count + repost_count + reply_count
```

---

## 3. Network Construction

The dataset was transformed into two main files:

* **Nodes** – representing X user accounts
* **Edges** – representing interactions between users

The network structure is represented as a **directed graph**, where each edge indicates the direction of interaction between users.

---

## 4. Social Network Analysis Metrics

Several centrality metrics were used to identify influential actors in the network:

### Degree Centrality

Measures the number of direct connections a node has.

### Betweenness Centrality

Identifies nodes that act as bridges connecting different parts of the network.

### Closeness Centrality

Measures how quickly a node can reach other nodes in the network.

### Eigenvector Centrality

Measures node influence based on the importance of connected nodes.

---

## 5. Network Visualization

Network visualization was conducted using **Gephi** with two layout approaches:

* **Out-Degree Contraction**
* **All-Degree Label Adjust**

Nodes were sized based on their degree values and colored to represent different clusters within the network.

---

# Results

The analysis shows several important findings:

## Passive Interaction Pattern

Most interactions occur through **likes and reposts**, indicating that users tend to participate passively rather than actively engaging in discussions.

## Centralized Network Structure

The network structure is **centralized**, meaning that only a small number of accounts dominate the flow of information.

## Key Actors

Several accounts were identified as key actors in the network:

* **na_na256** – highest degree centrality
* **bluetuwlips** – highest betweenness centrality
* **DroneEmpritofficial** – highest eigenvector centrality

These accounts play important roles either as **information spreaders or connectors between communities**.

## Fragmented Communities

The network also contains **smaller clusters** of users that are weakly connected to the main conversation, indicating fragmented community structures.

---

# Technologies Used

The analysis in this project uses the following tools and technologies:

* Python
* Pandas
* Social Network Analysis (SNA)
* Gephi
* Tweet Harvest
* Data Visualization

---

# Project Structure

```
IndonesiaGelap-Social-Network-Analysis
│
├── dataset
│   ├── Edges_Indonesia_Gelap_Final.csv
│   └── Nodes_Indonesia_Gelap_Final.csv
|   └── Data Mentah Indonesia_Gelap.csv
│
├── notebooks
│   ├── Tweet Harvest (X Twitter Data Crawling).ipynb
│   ├── Calculate_Centrality.ipynb
│   └── Code Deskripsi Data.ipynb
│
├── gephi_project
│   └── Tugas Akhir SNA.gephi
│
├── paper
│   └── final project 1 SNA.pdf
│
└── README.md
```

---

# Authors

* Senna Yoga Abira
* Aura Aulia Anastasya Hadi Putri
* Asyifa Izayani Safari

---

# Conclusion

This study demonstrates that the **#IndonesiaGelap discussion on X forms a centralized network with predominantly passive interaction patterns**. Although many users participate in the conversation, only a small number of accounts significantly influence the flow of information.

The findings highlight how **network structures and key actors play a crucial role in shaping information dissemination and public opinion within social media ecosystems**.
