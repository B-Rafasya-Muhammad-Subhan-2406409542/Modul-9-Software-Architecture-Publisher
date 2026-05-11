## Tutorial 9: Event-Driven Architecture (Publisher)

**a. How much data your publisher program will send to the message broker in one run?**
Program publisher akan mengirimkan 5 data (*event messages*) ke dalam antrean *message broker* dalam satu kali eksekusi, yaitu data atas nama Amir, Budi, Cica, Dira, dan Emir.

**b. The url of: "amqp://guest:guest@localhost:5672" is the same as in the subscriber program, what does it mean?**
Hal tersebut menandakan bahwa program *publisher* dan *subscriber* terhubung ke server *message broker* (RabbitMQ) yang sama persis. Karena mereka berada pada koneksi dan antrean (*queue*) yang sama, *publisher* dapat mengirimkan pesan yang kemudian dapat didengar (listen) dan dikonsumsi secara langsung oleh *subscriber*.

## RabbitMQ Overview
![RabbitMQ Overview](images/rabbitmq_running_overview.png)

## Event Processing Log
![Event Processing](images/event_processing_log.png)

## RabbitMQ Monitoring
![RabbitMQ Message Rate Graph](images/rabbitmq_monitoring_spike.png)
Lonjakan (spike) pada grafik menunjukkan momen ketika program publisher mengirimkan 5 pesan ke message broker. Karena pesan tersebut langsung dikonsumsi oleh subscriber, grafik kembali ke titik nol setelah proses selesai.