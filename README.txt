---Ciphix Dispatcher Framework
---Created on UiPath Studio version 4.1

This framework has been created with the purpose of alleviating time a developer has to spend on creating a Dispatcher for his/her process.
The framework is generic enough to add Transaction Items of dynamic sizes to an Orchestrator Queue.
Below is a step-by-step guide for correctly implementing the Dispatcher framework in your project.

1. Import the Dispatcher Framework
2. In the Config file, change the Value associated with OrchestratorQueueName to whatever name your Queue has
3. In the Data Retrieval State, fill dtTransactionData with all the data which will be sent to the Queue (through means of data scraping, reading a file, etc.).
   In the Dispatch State, the data within dtTransactionData will be added as Transaction Items where every row is a separate Transaction Item.
4. Before running your modified framework, ensure that you have a connection with your Orchestrator (check UiPath Robot)