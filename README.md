# Bro-Cut
Bro-cut is a command used to only show desired fields from Zeek logs. When Zeek logs are in CVS there is a lot of fields that are not relevant to searching for malicious activity. Showing only desired fields helps in making the data make more sense and easier to read. Below is an example of the conn.log in its raw format.


![conn.log picture](https://github.com/gageb1989/Bro-Cut/blob/main/pictures/Picture1.png)

## Using bro-cut

There are different ways to use the command but one way is to cat the log or zcat the log if it is zipped and pipe it to the bro-cut command. Below the image shows the same log file read with bro-cut using the following command: "cat conn.log | bro-cut ts -d id.orig_h id.orig_P id.resp_h id.resp_p proto service". 

![Second bro-cut picture](https://github.com/gageb1989/Bro-Cut/blob/main/pictures/Picture2.png)

## Why?
There are many data ingest tools that make reading data like Zeek logs easier like Splunk and Kibana. Sometimes there are situations especially in incident response when those tools are not available. If you understand the raw data then it does not matter what data ingest tool you are using. The bro-cut-command.md has a list of bro-cut commands I use frequently while hunting for malicious behavior. Having the commands ready for a quick copy and paste makes the job easier and success higher. 
