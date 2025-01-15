**Apache Spark** is an open-source distributed computing engine with in-memory processing. It has a three-layered architecture: The DRIVER node communicates with the CLUSTER MANAGER, responsible for creating WORKER nodes that execute multiple tasks and send the result to the driver. 

* Driver Node - It runs JVM. The driver initiates the spark session when the user submits the code. DAG scheduler creates a lineage graph and the actual data is processed only when the action command is called (Hence lazy evaluation). Task schedular communicates with the cluster manager in negotiating the resources and allocating jobs to the worker nodes. 

* Worker Node - Each worker node can have multiple executors same as each executor with multiple cores. Data can be stored either inside the on-heap memory as partitions or outside the JVM process, which is handled directly by the OS through off-heap memory. 
