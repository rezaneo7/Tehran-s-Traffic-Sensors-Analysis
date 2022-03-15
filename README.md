# Tehran Traffic Data Analysis

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)


<p align="center">
    <img 
    src="https://user-images.githubusercontent.com/31289283/158394938-ae889506-636b-43be-80c2-6fde63674242.jpg" 
    height=75% 
    width=75%
    >
</p>

**Data Analysis of Tehran's Traffic Data**
* Recommending new paths for each individual car using Frequent itemsets Algorithm (FP-Growth)
* Finding and clustring cars with similar driving patterns using LSH
* Finding important points( Traffic cameras ) using PageRank 
* Clustring Traffic cameras using Community Detections algorithm (GraphX) 
* Designing a Recommender System to suggest new paths using ALS


How to Use
==============
* Related articles are saved in Folders with the same name as Algorithm

* There are two code file :

-- 1) Project.ipynb : written in pyspark. Just upload it in Google Colab and run Sequentially. All needed Libraries are provided in the code( even installation of new ones )

-- 2) Scala_traffic.ipynb : written in scala+spark. again all libraries are included. Just Run each block of code sequentially
      
     Usage Guide for Scala:
	
	1) download docker using this command:
		docker pull jupyter/all-spark-notebook

	2) open powershell and use thic command:
 		docker run -it --rm -e SPARK_OPTS="--driver-memory 10g" -p 8888:8888 -p 4040:4040 -p 4041:4041 -e GRANT_SUDO=yes --user root -v X:/Path/to/code:/home/jovyan/workspace jupyter/all-spark-notebook
	
	pay attention, you should fill (X:/path/to/code) with correct directory of Scala_traffic.ipynb and also CSV file of dataset should be in the same folder.
	And you can specify driver memory base on your Ram ( I need large heap size for Strongly connected components, its default value is 1gig)

	3) then it starts and give you link of jupyter notebook which you can access code with.

	4) after running first cell of code and spark initialization completion, you can access SPARK UI with http://localhost:4040/

* I tried to load scala kernel(spylon-kernel) in colab, but i was'nt successful. So Only ways to test the code are wheter use docker or have spark and scala installed. 


