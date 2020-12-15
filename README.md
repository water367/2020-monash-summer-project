# 2020-monash-summer-project

this project is under supervision of Dr. Khalajzadeh &amp; Dr. Obie in monash university

# Detecting values-violating defects in source code (mobile apps)

### program structure

#### 1. repository_query
collect data from GitHub by GitHub Api;
data of android projects contains 5 topics: finance education communication, fitness, health.
remove the android projects who obtain less than 6 java file only.

#### 2. repository_cleaning
wrangle code data in class level
it includes 6 elements: function name, class name, comments, string, extension name, variable name

#### 3. repository_tree
15 root APIs
categorize high-level APIs to different root APIs

#### 4. repository_visual
root APIs' extension number
root API tree
