# Spark SQL Big Data
<div align="justify">
Tugas ini merupakan bagian dari mata kuliah Big Data dan berfokus pada topik DataFrame dan Dataset pada Apache Spark.
</div>

## Spark Web UI
<img src="img/spark_web_ui.png"/>
<div align="justify">
Spark Web UI adalah antarmuka pengguna web untuk memantau dan menganalisis aplikasi Spark. Spark Web UI menyediakan informasi detail tentang aplikasi Spark yang sedang berjalan, seperti status aplikasi, daftar tugas dan lain-lain.
</div>

## Metode 1: Membuat DataFrame dengan objek list, schema dan default data types
<img src="img/metode_2.1.png"/>
<div>
<pre>
<code>
from pyspark import *
from pyspark.sql import *
spark = SparkSession.builder.appName("metode1").getOrCreate()
sc = spark.sparkContext
mylist = [(50, "DataFrame"),(60, "pandas")]
myschema = ['col1', 'col2']
df1 = spark.createDataFrame(mylist, myschema)
df1.show()
</code>
</pre>
<p align="justify">
PySpark untuk membuat sebuah DataFrame pada Spark. Proses yang terjadi meliputi impor modul-modul PySpark, pembuatan objek SparkSession dengan nama aplikasi "metode1", pembuatan objek SparkContext untuk menghubungkan Spark dengan cluster, pembuatan list yang berisi tuple data, pembuatan list yang berisi nama kolom, pembuatan objek DataFrame dengan metode createDataFrame(), dan terakhir memanggil metode show() pada objek DataFrame untuk menampilkan isi dari DataFrame.
</p>
</div>

