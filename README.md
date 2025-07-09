# Connectify- A Social Network Recommendation System
This project focuses on analyzing and cleaning data from a simulated social media platform. It demonstrates how to handle JSON data, clean inconsistencies, and implement recommendation systems like "People You May Know" and "Pages You May Like" using Python.

# 📁 Project Structure
<pre><code> 📦 Social Network Data Analysis ├── 📁 jupyter notebooks │ ├── 01_data_display.ipynb # Display users and pages │ ├── 02_data_cleaning.ipynb # Clean and validate data │ ├── 03_people_you_may_know.ipynb # Recommend friends │ └── 04_pages_you_may_like.ipynb # Recommend pages ├── 📁 data │ ├── data.json # Original dataset │ ├── data2.json # Dataset with errors │ ├── massive_data.json # Large dataset for testing │ └── cleaned_data2.json # Cleaned output dataset </code></pre>

# 🧠 Features Implemented

1. **Data Display (01_data_display.ipynb):**
   - Loads and parses JSON data for users and pages.
   - Displays user details including their friends and liked pages.
   - Displays the list of all available pages.

2. **Data Cleaning (02_data_cleaning.ipynb):**
   - Removes:
     - Users with missing names.
     - Duplicate friend entries.
     - Duplicate liked pages and page records.
     - Users with no friends and no liked pages (inactive users).
   - Ensures data consistency across users and pages.

3. **People You May Know (03_people_you_may_know.ipynb):**
   - Recommends friends to each user based on:
     - Mutual friends.
     - Excludes already connected users and the user themself.
     - Displays the number of mutual friends for each suggestion.

4. **Pages You May Like (04_pages_you_may_like.ipynb):**
   - Suggests new pages to a user by analyzing:
     - Pages liked by their friends.
     - Excludes pages already liked by the user.
     - Outputs the most recommended pages.

# 🧹 Sample Data Issues and Fixes
**Issues in data2.json:**
- Duplicate entries in the friends and pages arrays.
- Empty name fields.
- Pages with duplicate IDs and inconsistent names.

**Fixes in cleaned_data2.json:**
- Removed empty name users.
- Removed inactive users.
- Deduplicated friends and liked pages.
- Consolidated duplicate page entries.

# 🧪 Datasets
**data.json**
- Clean, small-scale dataset for testing features.

**data2.json**
- Contains deliberate errors for testing the cleaning module.

**massive_data.json**
- Large dataset (30 users, 27 pages) for scalability and performance testing.

# 🛠 Technologies Used
- **Language:** Python 3
- **Libraries:** json, collections, IPython.display
- **Tools:** Jupyter Notebook

# 📌 How to Run
1. Clone this repository.
2. Open the .ipynb files using Jupyter Notebook or VSCode with Python extension.
3. Follow the order:
   - Start with 01_data_display.ipynb to inspect the data.
   - Then run 02_data_cleaning.ipynb to clean the dataset.
   - Next, run 03_people_you_may_know.ipynb and 04_pages_you_may_like.ipynb for recommendations.

# ✅ Future Enhancements
- Add a simple web UI using Flask or Streamlit.
- Integrate visualizations for network graphs (using NetworkX).
- Export recommendations as downloadable reports.
- Add unit tests for data integrity validation.

## 👤 Author

**Aniruddha Gupta**  
**🎓 B.Tech in Computer Science Engineering**  
**🔧 Interests:** Backend Development • Data Analysis • Innovation
