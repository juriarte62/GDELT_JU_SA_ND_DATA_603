# GDELT_JU_SA_ND_DATA_603
This is the GitHub repository for the final group project for DATA 603. The primary contributors are Jonathan Uriarte, Sabri Amer, and Nick Devroye. 

We will be using data from the Global Database of Events, Language, and Tone (GDELT). 
Link to the website is here: [GDELT](https://www.gdeltproject.org/)



# Github link for GDELT 
There is a github repository to use the GDELT API: [GitHub GDELT Link](https://github.com/alex9smith/gdelt-doc-api)

# Conda Environment setup
## set up conda environment name
```
conda create -n spark_env python=3.10
conda activate spark_env
```

## Install JAVA to conda environment
```
conda install openjdk=17
# we are using JAVA version 17 for this apache spark download
```

## Install Apache Spark
```
# conda version
conda install pyspark
```
```
# pip version
pip install pyspark
```

## Test Apache Spark package in VS Code
```
from pyspark.sql import SparkSession

spark = SparkSession.builder \
    .master("local[*]") \
    .appName("TestSpark") \
    .config("spark.ui.enabled", "false") \
    .config("spark.driver.bindAddress", "127.0.0.1") \
    .getOrCreate()

print("✅ Spark started successfully!")
spark.stop()
```