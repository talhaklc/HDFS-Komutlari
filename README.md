# HDFS-Komutlari
Udemy Big Data Eğitim Seti için hazırlanan HDFS Komutları

HDFS için yazacağımız tüm komutlara 'hdfs dfs' ile başlayacağız.

//HDFS'de Klasör Oluşturma
Komut : hdfs dfs -mkdir /klasöradi
Örnek : hdfs dfs -mkdir /example

//Local Makinedeki Veriyi HDFS'e Kopyalama
Komut : hdfs dfs -copyFromLocal /localdeki-kaynak-klasör /hedef-hdfs-klasörü
Örnek : hdfs dfs -copyFromLocal /home/cloudera/Desktop/ratings.csv /example

//Klasörde Bulunan Dosya Sayısını Öğrenme
Komut : hdfs dfs -count /hdfs-klasörü
Örnek : hdfs dfs -count /example

//Dosyanın İçeriğini Konsola Yazdırma
Komut : hdfs dfs -cat /hdfs-klasörü
Örnek : hdfs dfs -cat /example/ratings.csv

//HDFS'de Klasörler Arası Dosya Kopyalama
Komut : hdfs dfs -cp /kaynak-hdfs-klasörü /hedef-hdfs-klasörü
Örnek : hdfs dfs -cp /example/ratings.csv /var

//HDFS'de Klasörler Arası Dosya Taşıma
Komut : hdfs dfs -mv /kaynak-hdfs-klasörü /hedef-hdfs-klasörü
Örnek : hdfs dfs -mv /example/ratings.csv /var

//Klasör, Dosya Silme
Komut : hdfs dfs -rmr /hdfs-klasörü
Örnek : hdfs dfs -rmr /example

//Dizin İçeriğinde Bulunan Dosya İsimlerini Listeleme
Komut : hdfs dfs -ls /hdfs-dizini
Örnek : hdfs dfs -ls /user

//Klasör İzin Yönetimi
Komut : hdfs dfs -chmod +,-(x,w,r) /hdfs-klasörü
Örnek : hdfs dfs -chmod +x /user/ratings.csv  //ratings dosyasına çalıştırma izni ekler
Örnek2: hdfs dfs -chmod -w /user/ratings.csv  //ratings dosyasına yazma iznini kaldırır

//Replication Factor Belirleme
Komut : hdfs dfs -setrep RepDegeri -R /hdfs-klasörü
Örnek : hdfs dfs -setrep 4 -R /user/ratings.csv
