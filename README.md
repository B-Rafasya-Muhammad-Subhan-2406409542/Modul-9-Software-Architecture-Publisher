## Tutorial 9: Event-Driven Architecture (Publisher)

**a. How much data your publisher program will send to the message broker in one run?**
Program publisher akan mengirimkan 5 data (*event messages*) ke dalam antrean *message broker* dalam satu kali eksekusi, yaitu data atas nama Amir, Budi, Cica, Dira, dan Emir.

**b. The url of: "amqp://guest:guest@localhost:5672" is the same as in the subscriber program, what does it mean?**
Hal tersebut menandakan bahwa program *publisher* dan *subscriber* terhubung ke server *message broker* (RabbitMQ) yang sama persis. Karena mereka berada pada koneksi dan antrean (*queue*) yang sama, *publisher* dapat mengirimkan pesan yang kemudian dapat didengar (listen) dan dikonsumsi secara langsung oleh *subscriber*.