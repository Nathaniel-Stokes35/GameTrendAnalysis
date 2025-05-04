# Game Trends Analysis

Analyzed global video game sales for 2016 to identify regional trends and suggest genre prioritization, looking for "Big Winners" for upcoming 2017 demographics.

## 📁 Project Structure

datasets 
<ul>
  <li>games.csv</li>
</ul>
GameTrendAnalysis.ipynb

## 🚀 Purpose

Using Exploratory Data Analysis, analyze common game trends to better predict "Big Winners" for the following year.

---

## 🧩 Data Sources

Four CSV files found in the `datasets` folder:

- **games.csv** – Total game sales infomration dataset.

## 🔍 Initial Exploratory Data Analysis

Dataset containted name, platform, release year, genre, na, jp, and eu sales, critic scores, user scores, ratings, and total sales in millions.

findings:
  - User_scores and Critic_Scores were not heavy indicators of game performacnce.
  - Missing scores were presumably caused by the games predating common user review metrics.
  - age was a major determiner on preformance, favoring newer games.
  - Console life is 3 years from its peak.
  - Restricted data to last 6 years to reduce noise and improve preformance.

---

## 🧼 Preprocessing Highlights

- lowered all coloumn names for consistency in references
- filled 'year_of_release' missing values with '0' for generalization purposes
- converted 'user_score' to floats allowing stronger calculations
- filled missing 'rating' entries with 'unknown'.
- split data into most recent 6 years corelating with console life cycle observations.
- filled missing user_scores and critic_scores with the average mean within the genre of missing data game

---

## 📊 Visualization Insights

- The Xbox360 and PS3 were "on it's way out" in 2016; with their upgraded counterparts on the rise.
- PS2, PSV, DS, PSP, Wii, and WiiU preformed porrly, several with no sales in the last three years of the dataset completely.
- Critical Reviews have the most variance and are not a good indicator of a games success with a weak correlation between performance and scores.
- Variance in Sales between Genres are inconsistent, with some Genres having much more sporadic variance than others and the "shooters" genre having the greater liklihood of performing well.

---

## 🧠 Deeper Exploratory Data Analysis

### 📌 Comparing Specifics and Regional Trends

To identify how factors such as platform, genre, and ESRB rating influence regional sales, we performed the following key steps:

1. **Enhanced Data Consistency**
   Filled in missing ESRB ratings across platforms to ensure complete data coverage when analyzing game performance by region.

2. **Cross-Platform Aggregation**
   Consolidated sales data to represent total performance per game, rather than per platform, enabling a more accurate view of top-performing titles.

3. **Interactive Metrics Tool**
   Built an interactive chart to dynamically explore performance by metric, allowing easier updates and exploration during analysis.

---

### 🌍 Regional User Profiles

#### 🇺🇸 North America (NA)

North American gamers prefer fast-paced AAA titles, often favoring mature-rated games. Franchises like *Grand Theft Auto*, *Call of Duty*, and *Skyrim* dominate, highlighting a preference for action-heavy, high-budget experiences.

* **Top 5 Platforms** (2016 total sales):

  1. Xbox 360: \$334.18M
  2. PlayStation 3: \$229.25M
  3. Wii: \$121.20M
  4. PlayStation 4: \$108.74M
  5. Xbox One: \$93.12M

* **Top 5 Genres**:

  1. Action: \$290.64M
  2. Shooter: \$237.47M
  3. Sports: \$156.81M
  4. Miscellaneous: \$123.80M
  5. Role-Playing: \$112.05M

#### 🇪🇺 Europe (EU)

European gamers share similarities with North American players but show greater favor toward family-friendly and sports titles (notably *FIFA*). ESRB ratings appear to hold more influence compared to NA.

* **Top 5 Platforms**:

  1. PlayStation 3: \$213.60M
  2. Xbox 360: \$163.41M
  3. PlayStation 4: \$141.09M
  4. PC: \$68.82M
  5. Wii: \$65.91M

* **Top 5 Genres**:

  1. Action: \$233.63M
  2. Shooter: \$171.45M
  3. Sports: \$116.84M
  4. Role-Playing: \$75.48M
  5. Miscellaneous: \$66.09M

#### 🇯🇵 Japan (JP)

Japan shows unique trends—favoring handheld platforms and role-playing games. ESRB ratings appear to carry more weight in purchasing decisions, with players exhibiting more selective spending behavior.

* **Top 5 Platforms**:

  1. Nintendo 3DS: \$100.62M
  2. PlayStation 3: \$59.26M
  3. PSP: \$42.20M
  4. Nintendo DS: \$27.90M
  5. PS Vita: \$21.84M

* **Top 5 Genres**:

  1. Role-Playing: \$103.54M
  2. Action: \$72.20M
  3. Miscellaneous: \$24.29M
  4. Platform: \$15.81M
  5. Adventure: \$15.67M

---

## 📈 Key Takeaways

* **Console Lifecycle** plays a major role in platform performance; most consoles show peak activity within a 3-year window.
* **Genre Trends** vary significantly by region—RPGs dominate Japan, while Action and Shooters thrive in NA and EU.
* **ESRB Ratings** appear to impact buying behavior more in Japan and Europe than in North America.
* **Critic and User Scores** do not show a strong correlation with actual sales performance.

---

## ✅ Final Thoughts

This project aimed to explore historical game sales and performance across platforms and regions to better predict successful genres and platforms for the upcoming 2017 market. Through robust EDA and preprocessing, we constructed regional user profiles and sales predictors to guide future development and marketing strategies for game developers and publishers.

---

## 💡 Future Improvements

* Incorporate **2017 sales data** (if available) to validate predictions.
* Develop a **predictive model** using regression or classification based on the EDA insights.
* Expand analysis to include **mobile platforms** or **emerging markets**.

---
