#                                                           Amazon_Vine_Analysis

Overview of the analysis: 

    In this project given to do is to use amazom rwd and as well s3.We will be able to ETL process to extract the dataset, transform the data, connect to an AWS RDS. we will use a file to grab the information that we will be using to use on google colab notebook.Here we are going to be doing the following of the steps:
    
    Deliverable 1: Perform ETL on Amazon Product Reviews
    Deliverable 2: Determine Bias of Vine Reviews
    Deliverable 3: A Written Report on the Analysis (README.md)
  
  Results:
  
    in this part with the file given to us to extract the information we had to create data frame for both challange "amazon ETL and as well on the amazon vine. ont the first amazon etl data frame it was the customers table 
    +-----------+--------------+
|customer_id|customer_count|
+-----------+--------------+
|   48670265|             1|
|   49103216|             2|
|    1131200|             1|
|   43076447|             2|
|   46261368|             1|
|    4883305|             5|
|   41192649|             1|
|   40985731|             7|
|   10437900|             2|
|   22245671|             1|
|    2574873|             1|
|    4696154|             1|
|    5621202|             1|
|    5871933|             2|
|   44089812|             1|
|    2845910|             1|
|    5274369|             1|
|   39069693|             2|
|     137793|             1|
|   31914942|             3|
+-----------+--------------+
only showing top 20 rows


the seconnd data frame was the products_table here is a picture of the data fram

+----------+--------------------+
|product_id|       product_title|
+----------+--------------------+
|B00CJ7IUI6|The Elder Scrolls...|
|B00DHF39KS|Wolfenstein: The ...|
|B00MUTAVH6|Under Night In-Bi...|
|B001AZSEUW|              Peggle|
|B00KVOVBGM|PlayStation 4 Con...|
|B00O9VGH4Y|USPRO&reg; Headph...|
|B004OQNZY4|Phineas and Ferb:...|
|B00ZLN980O|Donop seablue 2.4...|
|B002L8W5V6|Dotop Nintendo Ga...|
|B007AJZ5PY|Nyko Game Case fo...|
|B000AOEU2K|Fire Emblem: Path...|
|B000H8BW7U|Tanarus (PC) (Com...|
|B013RADQOQ|Susenstone® 2400D...|
|B00KQXKUJ2|FIFA 15 (Ultimate...|
|B006W41X2C|Turtle Beach - Ea...|
|B000KCX9M4|Grand Theft Auto:...|
|B00YT90JWC|Red Wii Mini Cons...|
|B0096KG6A8|Wii U Super Mario...|
|B00L6AVLB0|World of Tanks-X3...|
|B000IMYKQ0|Wii Nunchuk Contr...|
+----------+--------------------+
only showing top 20 rows


the third table was the customers_table
+-----------+--------------+
|customer_id|customer_count|
+-----------+--------------+
|   48670265|             1|
|   49103216|             2|
|    1131200|             1|
|   43076447|             2|
|   46261368|             1|
|    4883305|             5|
|   41192649|             1|
|   40985731|             7|
|   10437900|             2|
|   22245671|             1|
|    2574873|             1|
|    4696154|             1|
|    5621202|             1|
|    5871933|             2|
|   44089812|             1|
|    2845910|             1|
|    5274369|             1|
|   39069693|             2|
|     137793|             1|
|   31914942|             3|
+-----------+--------------+
only showing top 20 rows

This are samples of three data frames from the amazon etl.

How many Vine reviews and non-Vine reviews were there?
#question #5
paid_count = paid_vine_review_df.count()
paid_count
94
#Question#5
unpaid_count = unpaid_vine_df.count()
unpaid_count
40471

How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

#Question5
paid_5_count = paid_vine_review_df.filter("star_rating == 5").count()
paid_5_count
48

unpaid_5_count = unpaid_vine_df.filter("star_rating == 5").count()
unpaid_5_count
15663

What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
percentage_paid_count = paid_5_count/paid_count*100
51.06382978723404

percentage_unpaid = unpaid_5_count/unpaid_count*100
38.701786464381904

Summary:
In my oppion i dont see posistive bias in the first glare but if if we keep working on it to provide more information we can see that there are more people give their riview from the unpaid vines. as we can see on the unpaid_5_count it has 15663 then the Pid couont with it only haas 94
maybe doing a survey to the loyal customers would be another way to do more reaserch
