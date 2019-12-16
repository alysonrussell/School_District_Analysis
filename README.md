# School_District_Analysis

## Project Overview
Data was gathered from the school level and the student level in order to analyze test scores based on school size and budgets.  Analysis was performed in Jupyter Notebook using Python and the Pandas dependency.

### Data Cleaning
Data was modified to remove errors caused by missing grades, as well as to remove the test scores from 9th graders at Thomas High School based on information that this data was unreliable.  Student names were cleaned of any inaccurate prefixes or suffixes in order to match the student name with their official student records.


## Final Data
An analysis of the final data started with a basic overview of the scope of information we had available to us.

| Total Schools | Total Students | Total Budget | Average Math Score | Average Reading Score | % Passing Math | % Passing Reading | % Overall Passing |
|:-------------:|:--------------:|:------------:|:------------------:|:---------------------:|:--------------:|:-----------------:|:-----------------:|
|       15      |     39,170     |  $24,649,428 |        78.9        |          81.9         |       74%      |        85%        |        79%        |

From here, we started to look at specific trends based on other differences between the schools' size and budgets.  We were able to sort and view the top 5 schools based on the Overall Passing %:

### Top Five Schools
| School Name         | School Type | Total Students | Total School Budget | Per Student Budget | Average Math Score | Average Reading Score | % Passing Math | % Passing Reading | % Overall Passing | Spending Ranges (Per Student) | School Size        |
|---------------------|-------------|----------------|---------------------|--------------------|--------------------|-----------------------|----------------|-------------------|-------------------|-------------------------------|--------------------|
| Cabrera High School | Charter     | 1858           | $1,081,356.00       | $582.00            | 83.1               | 84.0                  | 94%            | 97%               | 96%               | <$584                         | Medium (1000-2000) |
| Pena High School    | Charter     | 962            | $585,858.00         | $609.00            | 83.8               | 84.0                  | 95%            | 96%               | 95%               | $585-629                      | Small (<1000)      |
| Griffin High School | Charter     | 1468           | $917,500.00         | $625.00            | 83.4               | 83.8                  | 93%            | 97%               | 95%               | $585-629                      | Medium (1000-2000) |
| Wilson High School  | Charter     | 2283           | $1,319,574.00       | $578.00            | 83.3               | 84.0                  | 94%            | 97%               | 95%               | <$584                         | Large (2000-5000)  |
| Wright High School  | Charter     | 1800           | $1,049,400.00       | $583.00            | 83.7               | 84.0                  | 93%            | 97%               | 95%               | <$584                         | Medium (1000-2000) |

We also looked at the bottom 5 schools to see how their metrics compared:

### Bottom Five Schools
| School Name           | School Type | Total Students | Total School Budget | Per Student Budget | Average Math Score | Average Reading Score | % Passing Math | % Passing Reading | % Overall Passing | Spending Ranges (Per Student) | School Size        |
|-----------------------|-------------|----------------|---------------------|--------------------|--------------------|-----------------------|----------------|-------------------|-------------------|-------------------------------|--------------------|
| Thomas High School    | Charter     | 1635           | $1,043,130.00       | $638.00            | 83.4               | 83.9                  | 67%            | 70%               | 68%               | $630-644                      | Medium (1000-2000) |
| Rodriguez High School | District    | 3999           | $2,547,363.00       | $637.00            | 76.8               | 80.7                  | 66%            | 80%               | 73%               | $630-644                      | Large (2000-5000)  |
| Figueroa High School  | District    | 2949           | $1,884,411.00       | $639.00            | 76.7               | 81.2                  | 66%            | 81%               | 73%               | $630-644                      | Large (2000-5000)  |
| Huang High School     | District    | 2917           | $1,910,635.00       | $655.00            | 76.6               | 81.2                  | 66%            | 81%               | 74%               | $645-675                      | Large (2000-5000)  |
| Johnson High School   | District    | 4761           | $3,094,650.00       | $650.00            | 77.0               | 81.0                  | 66%            | 81%               | 74%               | $645-675                      | Large (2000-5000)  |

Based on these results, we also started looking at results by grade, and results by Spending Ranges and School Size.

### Spending Ranges
| Spending Ranges (Per Student) | Average Math Score | Average Reading Score | % Passing Math | % Passing Reading | % Overall Passing |
|-------------------------------|--------------------|-----------------------|----------------|-------------------|-------------------|
| <$584                         | 83.5               | 83.9                  | 93%            | 97%               | 95%               |
| $585-629                      | 81.9               | 83.2                  | 87%            | 93%               | 90%               |
| $630-644                      | 78.5               | 81.6                  | 67%            | 77%               | 72%               |
| $645-675                      | 77.0               | 81.0                  | 66%            | 81%               | 74%               |

### School Size
| School Size        | Average Math Score | Average Reading Score | % Passing Math | % Passing Reading | % Overall Passing |
|--------------------|--------------------|-----------------------|----------------|-------------------|-------------------|
| Small (<1000)      | 83.8               | 83.9                  | 94%            | 96%               | 95%               |
| Medium (1000-2000) | 83.4               | 83.9                  | 88%            | 91%               | 90%               |
| Large (2000-5000)  | 77.7               | 81.3                  | 70%            | 83%               | 76%               |

### School Type
| School Type | Average Math Score | Average Reading Score | % Passing Math | % Passing Reading | % Overall Passing |
|-------------|--------------------|-----------------------|----------------|-------------------|-------------------|
| Charter     | 83.5               | 83.9                  | 90%            | 93%               | 92%               |
| District    | 77.0               | 81.0                  | 67%            | 81%               | 74%               |


## Affect of removing test scores from Thomas High School
Based on information that test scores from the ninth grade were altered, we removed these numbers from our calculations.  The below notates what was affected by this omission.

### District Summary
This slightly lowered the Average Scores and % Passing for all subjects.  % Overall Passing went from 80% to 79%.

### School Summary
This would have affected only the metrics for Thomas High School.  Removing these altered scores moved Thomas High School from one of the top 5 schools to the bottom 5 schools in the dataset.  The percentage passing for each subject as well as the % Overall Passing were significantly impacted.

This subsequently negatively affected the same metrics for the School Spending, School Type, and School Size analyses where Thomas High School was sorted.  ($630-$644 spending range, charter school type, and medium school size.)
