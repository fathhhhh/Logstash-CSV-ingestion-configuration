# Logstash-CSV-ingestion-configuration
This is example configuration template to ingest csv file to elasticsearch. The configuration divided into three part which is "input","filter" and "output"
The first part are the path that you put your location of your csv file. The second part where you put your column name and how you want to ingest and modify your output,
and the last one are for assign elasticsearch credential and index name.
How ?

1. Open your csv file with your text editor and look at the first line, here your column name.

![image](https://user-images.githubusercontent.com/67633326/193715183-9c3d7ca5-6b03-41fd-ab5f-e41d34592cba.png)

2. Your CSV file location 

![image](https://user-images.githubusercontent.com/67633326/193716398-582d5148-7c41-4fd2-8fa2-2f198b531997.png)

3. On the filter part, put your columns name

![image](https://user-images.githubusercontent.com/67633326/193715826-13e30d9d-e476-47c3-8a16-41c24e0a9ebd.png)

4. If you enable TLS uncomment the line and fill it with your config

![image](https://user-images.githubusercontent.com/67633326/193715573-9027664b-1973-410e-a9b8-86778e77a0c8.png)

5. Test your configuration file 
 /usr/share/logstash/bin/logstash --config.test_and_exit -f /etc/logstash/conf.d/csv.conf
6. Restart your logstash
