# HDFS Testing

## Teragen
```bash
[cate@ip-172-31-15-167 ec2-user]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -D dfs.blocksize=16M -D mapreduce.map.memory.mb=512 65536000 /user/cate/tgen
17/05/05 05:07:16 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-10-217.eu-central-1.compute.internal/172.31.10.217:8032
17/05/05 05:07:17 INFO terasort.TeraGen: Generating 65536000 using 2
17/05/05 05:07:17 INFO mapreduce.JobSubmitter: number of splits:2
17/05/05 05:07:17 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1493973840400_0001
17/05/05 05:07:18 INFO impl.YarnClientImpl: Submitted application application_1493973840400_0001
17/05/05 05:07:18 INFO mapreduce.Job: The url to track the job: http://ip-172-31-10-217.eu-central-1.compute.internal:8088/proxy/application_1493973840400_0001/
17/05/05 05:07:18 INFO mapreduce.Job: Running job: job_1493973840400_0001
17/05/05 05:07:24 INFO mapreduce.Job: Job job_1493973840400_0001 running in uber mode : false
17/05/05 05:07:24 INFO mapreduce.Job:  map 0% reduce 0%
17/05/05 05:07:44 INFO mapreduce.Job:  map 21% reduce 0%
17/05/05 05:07:50 INFO mapreduce.Job:  map 27% reduce 0%
17/05/05 05:07:56 INFO mapreduce.Job:  map 32% reduce 0%
17/05/05 05:08:02 INFO mapreduce.Job:  map 38% reduce 0%
17/05/05 05:08:08 INFO mapreduce.Job:  map 44% reduce 0%
17/05/05 05:08:14 INFO mapreduce.Job:  map 49% reduce 0%
17/05/05 05:08:20 INFO mapreduce.Job:  map 55% reduce 0%
17/05/05 05:08:26 INFO mapreduce.Job:  map 60% reduce 0%
17/05/05 05:08:32 INFO mapreduce.Job:  map 66% reduce 0%
17/05/05 05:08:38 INFO mapreduce.Job:  map 72% reduce 0%
17/05/05 05:08:44 INFO mapreduce.Job:  map 78% reduce 0%
17/05/05 05:08:50 INFO mapreduce.Job:  map 83% reduce 0%
17/05/05 05:08:56 INFO mapreduce.Job:  map 89% reduce 0%
17/05/05 05:09:02 INFO mapreduce.Job:  map 95% reduce 0%
17/05/05 05:09:08 INFO mapreduce.Job:  map 100% reduce 0%
17/05/05 05:09:09 INFO mapreduce.Job: Job job_1493973840400_0001 completed successfully
17/05/05 05:09:09 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=249962
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=170
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=8
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=4
        Job Counters
                Launched map tasks=2
                Other local map tasks=2
                Total time spent by all maps in occupied slots (ms)=201877
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=201877
                Total vcore-seconds taken by all map tasks=201877
                Total megabyte-seconds taken by all map tasks=206722048
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=170
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1298
                CPU time spent (ms)=94180
                Physical memory (bytes) snapshot=309833728
                Virtual memory (bytes) snapshot=2289999872
                Total committed heap usage (bytes)=391118848
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000

				 

```
##Time

```bash
real    1m54.638s
user    0m5.939s
sys     0m0.251s
```

## Listing
```bash
[cate@ip-172-31-15-167 ec2-user]$ hdfs dfs -ls /user/cate/tgen
Found 3 items
-rw-r--r--   3 cate cate          0 2017-05-05 05:09 /user/cate/tgen/_SUCCESS
-rw-r--r--   3 cate cate 3276800000 2017-05-05 05:09 /user/cate/tgen/part-m-00000
-rw-r--r--   3 cate cate 3276800000 2017-05-05 05:09 /user/cate/tgen/part-m-00001

```