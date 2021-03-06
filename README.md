# JMeter for Dremio

Apache JMeter is an Apache project that can be used as a load testing tool for analyzing and measuring the performance of a variety of services.

This document describes how to configure, run and analyze the results of a JMeter test plan for Dremio.


### Download Dremio’s JDBC Driver
Download the latest jdbc driver from Dremio's website: https://www.dremio.com/drivers/jdbc

### Download & Install JMeter
> _JMeter requires Java 8 or higher_

Download the binaries: https://jmeter.apache.org/download_jmeter.cgi
1. Extract the binaries to a directory
2. Copy the Dremio Test Plan configuration file (dremio_testplan.jmx) to this directory
3. Now launch JMeter from the bin/ directory by executing ./jmeter.sh
4. File > Open > navigate to the directory containing the tp_config.jmx file
5. In the JDBC Connection Configuration tab > modify the Database URL: 

      - `direct`= <Hostname/IP address for the Dremio Coordinator Node>
      - `Port#`= <default is 31010>
      - `user`= <Dremio_user>
      - `password`= <Dremio_user password>
      - `schema`= optional - you can list it here or fully qualify the dataset name in the SQL

_(jdbc:dremio:direct=44.123.12.103:31010;user=admin;password=admin123)_





