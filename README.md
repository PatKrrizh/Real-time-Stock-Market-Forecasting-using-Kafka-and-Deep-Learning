# Real-time Stock Market Prediction using Kafka and Deep Learning
<i>“Data is the new science; big data holds the answers”!</i> - Pet Gelsinger!

The stock market is a complex non-linear dynamic system. Nowadays Financial Markets produce data at an astonishing speed from different sources. A competent system is required that can act immediately and produce results on the fly is expected to manage this steadily incoming data with minimal effort.

In this project, as a response to the requirements, I developed a Real-Time Stock Market Data Processing and Prediction application that includes the following features:
- Extraction of financial market data from Alpha Vantage API by making API calls.
- Use of Apache Kafka to stream real-time data between internal components of an application.
- Implementation of Long Short-Term Memory (LSTM) neural network model.
- Performing model training, testing and validation.
- Performing a real-time prediction of future price movement of various equity stocks (whether the value will drive up, down or stand).

Data Provider: [Alpha Vantage](https://www.alphavantage.co/)

# Architecture
![Architecture](https://github.com/PatKrrizh/Real-time-Stock-Market-Forecasting-using-Kafka-and-Deep-Learning/blob/main/Architecture.png)

### Installation

#### Apache Kafka:
- Download Apache Kafka
  - https://www.apache.org/dyn/closer.cgi?path=/kafka/2.7.0/kafka_2.13-2.7.0.tgz
- Open terminal and run the following code to install Apache Kafka for Python:
  - `~$pip install kafka-python`

#### Alpha Vantage:
- Link to Alpha Vantage:
  - https://www.alphavantage.co/

- Register yourself to Alpha Vantage to get the API Key.
- Open terminal and run the following code to install Alpha Vantage Module:
  - `~$pip install alpha_vantage`

### Usage:
- Unpack downloaded Kafka Repository to a specific path.
- Before every execution of the application, we must start the Zookeeper and Kafka brokers using the terminal:
  - From the root of Apache Kafka folder, run the following command in terminal to start Zookeeper:
    - `~$sh bin/zookeeper-server-start.sh config/zookeeper.properties`
  - Open another Terminal and run the following command from the root of Apache Kafka folder to start Apache Kafka broker.
    - `~$sh bin/kafka-server-start.sh config/server.properties`
- Create Kafka topics if running the application for the first time:
  - Create topic:
    - `$bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 3 --partitions 1 --topic topic_name`
  - List available topics:
    - `$bin/kafka-topics.sh --list --bootstrap-server localhost:9092`
- Specify your configuration of Apache Kafka and Alpha Vantage API key by modifying the following files:
  - [producer_first_time.ipynb](https://github.com/PatKrrizh/Real-time-Stock-Market-Forecasting-using-Kafka-and-Deep-Learning/blob/main/producer_first_time.ipynb) file
  - [producer.ipynb](https://github.com/PatKrrizh/Real-time-Stock-Market-Forecasting-using-Kafka-and-Deep-Learning/blob/main/producer.ipynb) file
  - [consumer.ipynb](https://github.com/PatKrrizh/Real-time-Stock-Market-Forecasting-using-Kafka-and-Deep-Learning/blob/main/consumer.ipynb) file
- Now we can run [producer_first_time.ipynb](https://github.com/PatKrrizh/Real-time-Stock-Market-Forecasting-using-Kafka-and-Deep-Learning/blob/main/producer_first_time.ipynb) file (if running the code for the first time) or producer.py to fetch financial data and send it to Kafka broker.
- Run [consumer.ipynb](https://github.com/PatKrrizh/Real-time-Stock-Market-Forecasting-using-Kafka-and-Deep-Learning/blob/main/consumer.ipynb) file to fetch data from Kafka broker.
- [basic_model.ipynb](https://github.com/PatKrrizh/Real-time-Stock-Market-Forecasting-using-Kafka-and-Deep-Learning/blob/main/basic_model.ipynb) file contains the model training for basic LSTM Model.
- Technical_model.py file contains the model training for Technical LSTM Model.
- To make a real-time prediction run [predict.ipynb](https://github.com/PatKrrizh/Real-time-Stock-Market-Forecasting-using-Kafka-and-Deep-Learning/blob/main/predict.ipynb) file.

