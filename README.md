# Course Analysis

This project presents a comprehensive analysis of Coursera course data, exploring course characteristics, popularity metrics, and organizational excellence. Through statistical analysis and data visualization, we uncover patterns and insights to help learners find the right courses and understand what makes courses successful on the Coursera platform.

> **Note**: This analysis contains interactive visualizations created with Plotly. These charts are fully interactive in Jupyter Notebook but may not display properly when viewed on GitHub.
## Dataset Overview

The analysis examines Coursera course data through multiple dimensions:
- Course ratings and enrollment numbers
- Difficulty levels (Beginner, Intermediate, Advanced)
- Certificate types (Specialization, Professional Certificate, Course)
- Course organizations (universities and companies)
- Student enrollment metrics

## Data Preparation and Cleaning

The data preparation process involved several key steps:

1. **Initial Data Assessment**
   - Verified data completeness with no missing values
   - Confirmed absence of duplicate entries
   - Converted student enrollment values from shorthand (k, m) to numerical format

2. **Outlier Analysis**
   - Implemented 1.5*IQR method for outlier detection in enrollment data
   - Identified courses with abnormally high enrollments
   - Retained outliers for analysis as they represent important trends in course popularity

## Key Findings

### Course Ratings Analysis
- Most courses are highly rated, with the majority falling in the 4.6-4.7 range (419 courses)
- No significant correlation between course ratings and enrollment numbers
- Analysis of top-rated courses across different certificate types

### Difficulty Level Insights
- Beginner courses dominate with 487 different offerings and nearly 40 million enrollments
- Intermediate courses represent a moderate portion of the catalog
- Advanced courses are significantly underrepresented with only 19 courses and 1.26 million enrollments

### Institutional Excellence
- The University of Chicago excels in beginner courses with highest ratings
- Stanford University leads in mixed-difficulty courses with largest enrollment among top-rated providers
- Duke University dominates the advanced course category with highest ratings

### Popular Specializations
- "Python for Everybody" by University of Michigan (4.8 rating)
- "Deep Learning" by deeplearning.ai (4.8 rating)
- "Improve Your English Communication Skills" by Georgia Institute of Technology (4.7 rating)

### Professional Certificates
- "SAS Programmer" by SAS
- "Google IT Support" by Google
- "Cloud Engineering with Google Cloud" by Google

### Top Individual Courses
- "Machine Learning" by Stanford University
- "The Science of Well-Being" by Yale University
- "Neural Networks and Deep Learning" by deeplearning.ai

## Technical Implementation

The analysis utilizes Python with key libraries:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px
import scipy
```

### Key technical features:
- Pandas for data manipulation and aggregation
- Plotly Express for interactive visualizations
- Statistical methods for correlation analysis
- Data transformation techniques for enrollment metrics

## Getting Started

1. Clone this repository
2. Install required dependencies:
   ```
   pip install pandas numpy matplotlib seaborn plotly scipy
   ```
3. Load the dataset:
   ```python
   df = pd.read_csv("coursea_data.csv")
   ```

## Data Structure

**Categorical Features**
- course_title: Name of the course
- course_organization: University or company offering the course
- course_Certificate_type: Type of certificate offered
- course_difficulty: Level of difficulty (Beginner, Intermediate, Advanced)

**Numerical Features**
- course_rating: Rating of the course (typically 1-5 scale)
- course_students_enrolled: Number of students enrolled in the course

## Visualizations

The project includes interactive visualizations:
- Distribution of course ratings
- Course counts and enrollment by difficulty level
- Top-rated organizations by difficulty level
- Top courses by certificate type and popularity

## Conclusion

The analysis reveals clear market preferences for beginner content and opportunities for growth in advanced courses. Educational institutions can leverage these insights to expand their online presence, while learners can identify high-quality content across different domains and difficulty levels.

## Suggestions for Improvement

Several improvements could enhance the depth and utility of this analysis:

1. **Time-Based Analysis**:
   - Data by year could show the track of enrollment trends over time
   - Would enable analysis of how course ratings evolve after launch
   - Possible identification of seasonal patterns in enrollment that could guide course release timing

2. **Completion rate**:
   - The course completion rate would show the course difficulty level and overall its quality 
   - Course duration data would show the relationship between length and popularity
   - Would show how the rate of the course changes based on its length
   
3. **Pricing and financial**: 
   - Would show how the price impacts popularity
   - Additional information would allow to see relations between price and rating 
   - Would allow better understanding of investments in studies 

4. **Visualization Enhancements**:
   - Creation of interactive dashboards would allow users to filter and explore data based on their interests
   - Course recommendation tool based on user needs and interest fields
