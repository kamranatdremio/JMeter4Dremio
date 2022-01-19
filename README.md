Apache JMeter is an Apache project that can be used as a load testing tool for analyzing and measuring the performance of a variety of services.

This document describes how to configure, run and analyze the results of a JMeter test plan for Dremio.

Download Dremio’s JDBC Driver
Download the latest jdbc driver: https://www.dremio.com/drivers/jdbc

Download & Install JMeter
JMeter requires Java 8 or higher
Download the binaries: https://jmeter.apache.org/download_jmeter.cgi
1. Extract the binaries to a directory
2. Copy the Dremio Test Plan configuration file (tp_config.jmx) to this directory
3. Now launch JMeter from the bin/ directory by executing ./jmeter.sh
4. File > Open > navigate to the directory containing the tp_config.jmx file
5. In the JDBC Connection Configuration tab > modify the Database URL: 
            direct= <Hostname/IP address for the Dremio Coordinator Node>
            Change the Port# is needed (default is 31010)
            user= <Dremio user>
            password= <Dremio user password>
            schema= <optional - you can list it here or fully qualify the dataset name in the SQL>




