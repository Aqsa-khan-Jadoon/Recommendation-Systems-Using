# 📚 Book Recommender System Using PySpark 🚀

## ✨ Overview
This project implements a **book recommendation system** using **Apache Spark's MLlib** in **PySpark**. The system includes multiple recommendation techniques such as:
- 🔹 **User-Based Collaborative Filtering**
- 🔹 **Item-Based Collaborative Filtering**
- 🔹 **Slope One Algorithm**
- 🔹 **ALS (Alternating Least Squares)**

The project also covers **data preprocessing** and **Spark session initialization** with optimized memory allocation.

---

## 🌟 Features
✅ Implements **four types** of recommendation algorithms
✅ Uses **PySpark's MLlib** for efficient large-scale computation
✅ **Preprocesses** data for optimal performance
✅ **Optimized Spark session** for distributed processing

---

## 🔧 Prerequisites
Make sure you have the following installed before running the project:
🟢 Python 3.x  
🟢 Apache Spark  
🟢 PySpark  
🟢 Jupyter Notebook (optional, for interactive exploration)  

---

## 🛠 Installation
1️⃣ Clone the repository:
   ```sh
   git clone https://github.com/yourusername/recommender-system-pyspark.git
   cd recommender-system-pyspark
   ```
2️⃣ Install dependencies:
   ```sh
   pip install pyspark
   ```

---

## ▶️ Usage
1️⃣ Start a Jupyter Notebook:
   ```sh
   jupyter notebook
   ```
2️⃣ Open `Recommender System Using Pyspark.ipynb` and **execute the cells sequentially**.
3️⃣ Modify parameters as needed to test different recommendation settings.

---

## 📂 Dataset
The model requires **book ratings data** in **CSV format**. The dataset should contain **user-item interactions**:
```
user_id, item_id, rating
1, 101, 5
2, 102, 3
...
```

📌 The following datasets are used:
- 🗂 `ratings.csv`: Contains user ratings for books.
- 📘 `books.csv`: Contains book metadata.

---

## ⚡ Spark Session Configuration
A **Spark session** is initialized with **optimized memory configurations** to handle large datasets efficiently:
```python
spark = SparkSession.builder.appName("BooksRecommendationSystem") \
    .config("spark.driver.memory", "8g") \
    .config("spark.executor.memory", "8g") \
    .config("spark.driver.maxResultSize", "4g") \
    .config("spark.memory.fraction", "0.8") \
    .config("spark.memory.storageFraction", "0.5") \
    .config("spark.sql.shuffle.partitions", "200") \
    .config("spark.dynamicAllocation.enabled", "true") \
    .config("spark.dynamicAllocation.initialExecutors", "2") \
    .config("spark.dynamicAllocation.minExecutors", "1") \
    .config("spark.dynamicAllocation.maxExecutors", "10") \
    .config("spark.serializer", "org.apache.spark.serializer.KryoSerializer") \
    .config("spark.shuffle.service.enabled", "true") \
    .config("spark.shuffle.compress", "true") \
    .config("spark.io.compression.codec", "snappy") \
    .getOrCreate()
```

---

## 🔍 Model Details
📌 **User-Based Collaborative Filtering** - Recommends books based on user similarities.  
📌 **Item-Based Collaborative Filtering** - Recommends books based on item similarities.  
📌 **Slope One Algorithm** - A simple yet effective rating prediction method.  
📌 **ALS (Alternating Least Squares)** - A matrix factorization approach for generating recommendations.  
🔹 Model **hyperparameters** such as **rank, iterations, and regularization** can be fine-tuned.  
🔹 The trained model can **predict ratings for unseen user-item pairs**.  

---

## 💡 Contributing
🎉 **Contributions are welcome!** Feel free to submit issues or pull requests to **enhance** the project.  

---

## 📜 License
This project is licensed under the **MIT License**. See `LICENSE` for details.  

🚀 **Happy Coding!** 🎯


