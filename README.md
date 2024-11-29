# Personal Dota 2 Data Analysis Project

---

## **Project Overview**
This project focuses on analyzing my personal Dota 2 gaming data to uncover patterns and insights into my gaming behavior. By exploring various aspects of my gameplay history, I aim to answer specific research questions that delve into hero preferences, performance trends, and factors affecting match outcomes. The data sources include my personal match history, official Dota 2 APIs, and web-scraped hero information from the Dota 2 website.

---

## **Data Collection**

### **1. Personal Match History**
- **Source:** Steam Web API  
- **Endpoint:**  
  ```
  https://api.steampowered.com/IDOTA2Match_570/GetMatchHistoryBySequenceNum/v1/?key={API_KEY}&start_at_match_seq_num={match_seq_num}
  ```
- **Collected Data:**
  - General match details:  
    - Duration, start time/date, winning team, game mode, total kills for both teams, tower status for both teams, match sequence number.
  - Player performance metrics:  
    - Kills, deaths, assists, gold per minute, XP per minute, last hits, denies, net worth, level, and team assignment.

### **2. General Game Information**
- **Source:** Official Dota 2 API  
- **Endpoints:**  
  - Items: [https://www.dota2.com/datafeed/itemlist?language=English](https://www.dota2.com/datafeed/itemlist?language=English)  
  - Heroes: [https://www.dota2.com/datafeed/herolist?language=English](https://www.dota2.com/datafeed/herolist?language=English)

### **3. Hero Characteristics**
- **Source:** Web scraping the Dota 2 website using Selenium.  
- **Collected Data:**  
  - Role distribution for each hero (carry, support, disabler, etc.).  
  - This data is used to analyze hero roles and their impact on my gameplay.

---

## **API and Permissions**
To retrieve my personal data:
- **Steam API Key:** Obtained from my Steam account.
- **Profile Configuration:**  
  - Profile and game details set to **public**.  
  - "Expose Public Match Data" enabled in Dota 2 game options.  
- **API Usage Limitations:**  
  - Steam API allows up to 100,000 calls per day ([Steam API Terms](https://steamcommunity.com/dev/apiterms)).  
  - I ensure compliance with privacy terms and avoid accessing confidential player data.  
- **Security:** My API key is excluded from the repository to maintain security.

---

## **Research Questions**
1. **Which type of heroes are best for me?**  
   - I will analyze the role distribution of heroes I play and compare my performance statistics across these roles to identify patterns and draw conclusions.

2. **Do I respect my role distribution in terms of my in-game item preferences?**  
   - I will evaluate if my item choices align with the roles assigned to the heroes I play.

3. **Does the number of matches played with a hero affect my experience/performance?**  
   - By examining performance trends over time, I will determine if playing more matches with a hero improves my gameplay.

4. **Does game duration affect my performance or match result?**  
   - I will analyze the correlation between match duration and performance metrics or win/loss outcomes.

5. **Does the number of games played in one sitting affect my performance or match result?**  
   - I will explore the relationship between the number of games played in a single session and my overall performance.

6. **Do starting time and date of matches affect my performance?**  
   - I will investigate how match timestamps influence my performance. For example:
     - Seasonal effects (e.g., summer or winter).
     - Specific periods (e.g., COVID-19 pandemic).

---

## **Motivation**
This project stems from my curiosity to understand my gaming patterns and improve my overall gameplay experience. By systematically analyzing data, I aim to uncover actionable insights that can enhance my performance and make my Dota 2 experience more enjoyable.

---

## **Tools and Methodology**
- **Programming Languages:** Python
- **Data Retrieval:** Steam Web API, Official Dota 2 API, and Selenium for web scraping.
- **Data Processing and Analysis:** Pandas and Matplotlib for data manipulation and visualization.
- **Security:** API keys are stored securely and not shared publicly.

---

## **Disclaimer**
All data collected and analyzed in this project complies with the terms and conditions of Steam and Dota 2. This project is for personal and educational purposes only, and no confidential or private information about other players is accessed or stored.

---

