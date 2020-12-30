# Simple Event Stream App	



![Diagram](images/diagram.png "Diagram")

Repository ini adalah sebagai bahan untuk mempelajari konsep dan cara kerja event stream architecture dengan real time case

1. ##### Producer

   Bertugas untuk generate nilai Long secara random dari angka 1 sampai 1000 kemudian mengirimkan data tersebut ke kafka dengan topic **numbers**

    

2. **Processor**

   Menerima data dari kafa dengan topic **numbers** kemudian memproses angkanya dengan melakukan filter angka genap dan melakukan operasi pengkalian v = v * v, kemudian mengirimkan kembali ke kafka dengan topic **squaredNumbers**

   

3. **Consumer**

   Menerima data dari kafka dengan topic **squaredNumbers** dan menampilkan dalam console.



**Prerequisites**

Sebelum mencoba repo ini pastikan local anda sudah terinstall :

1. OpenJDK 11
2. Kafka Local
3. Inteljidea atau Spring Tool Suite as IDE
4. Kafka Tool



Setelah anda menjalankan **zookeeper** dan **kafka server** nya buatlah dua topic berikut :

> kafka-topics --zookeeper 127.0.0.1:2181 --topic ***numbers*** --create --partitions 1 --replication-factor 1

> kafka-topics --zookeeper 127.0.0.1:2181 --topic ***squaredNumbers*** --create --partitions 1 --replication-factor 1



### **How to use it ?**

1. Pastikan zookeeper dan kafka server sudah running
2. Pastikan topic ***numbers***  dan ***squaredNumbers*** sudah dibuat
3. Running **app-producer**
4. Running **app-processor**
5. Running **app-consumer**



### **ScreenShoot**

![app-producer](images/app-processor.png "Producer")

![app-consumer](images/app-consumer.png "app-consumer")