# 🌐 Personal Developer Portfolio

> Personal portfolio website showcasing projects, skill sets, technical background, and contact avenues.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)

---

## ⭐ Star Schema (Portfolio Visitor Analytics)

```
                            +-----------------------------------+
                            |           Dim_Project             |
                            +-----------------------------------+
                            | Project_Key (PK)                  |
                            | Project_Title                     |
                            | Tech_Stack                        |
                            +-----------------+-----------------+
                                              | 1
                                              |
                                              | N
+-----------------------+   +-----------------+-----------------+   +-----------------------+
|  Dim_Calendar         | 1 |    Fact_PortfolioInteraction      | 1 |  Dim_VisitorRegion    |
+-----------------------+---+-----------------------------------+---+-----------------------+
| DateKey (PK)          | N | Interaction_Key (PK)              | N | Region_Key (PK)       |
| FullDate              |   | DateKey (FK)                      |   | Country               |
+-----------------------+   | Project_Key (FK)                  |   | City                  |
                            | Region_Key (FK)                   |   +-----------------------+
                            | Demo_Clicks_Count (Measure)       |
                            | Repo_Clicks_Count (Measure)       |
                            +-----------------------------------+
```
