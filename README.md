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
![Architecture](https://github.com/radoslawkrolikowski/financial-market-data-analysis/blob/master/assets/app-architecture.png)

### Installation

#### Apache Kafka:
- Download Apache Kafka
  - (https://www.apache.org/dyn/closer.cgi?path=/kafka/2.7.0/kafka_2.13-2.7.0.tgz)
- Open terminal and run the following code to install Apache Kafka for Python:
  - `~$pip install kafka-python`
