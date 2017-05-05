## Pi

```bash
[jemaine@ip-172-31-10-217 ec2-user]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 6 250
Number of Maps  = 6
Samples per Map = 250
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Wrote input for Map #5
Starting Job
17/05/05 05:46:11 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-10-217.eu-central-1.compute.internal/172.31.10.217:8032
17/05/05 05:46:11 INFO hdfs.DFSClient: Created token for jemaine: HDFS_DELEGATION_TOKEN owner=jemaine@SEBASTIANKRAMP.AU, renewer=yarn, realUser=, issueDate=1493977571919, maxDate=1494582371919, sequenceNumber=2, masterKeyId=2 on 172.31.10.217:8020
17/05/05 05:46:11 INFO security.TokenCache: Got dt for hdfs://ip-172-31-10-217.eu-central-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.10.217:8020, Ident: (token for jemaine: HDFS_DELEGATION_TOKEN owner=jemaine@SEBASTIANKRAMP.AU, renewer=yarn, realUser=, issueDate=1493977571919, maxDate=1494582371919, sequenceNumber=2, masterKeyId=2)
17/05/05 05:46:12 INFO input.FileInputFormat: Total input paths to process : 6
17/05/05 05:46:12 INFO mapreduce.JobSubmitter: number of splits:6
17/05/05 05:46:12 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1493976887575_0002
17/05/05 05:46:12 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.10.217:8020, Ident: (token for jemaine: HDFS_DELEGATION_TOKEN owner=jemaine@SEBASTIANKRAMP.AU, renewer=yarn, realUser=, issueDate=1493977571919, maxDate=1494582371919, sequenceNumber=2, masterKeyId=2)
17/05/05 05:46:13 INFO impl.YarnClientImpl: Submitted application application_1493976887575_0002
17/05/05 05:46:13 INFO mapreduce.Job: The url to track the job: http://ip-172-31-10-217.eu-central-1.compute.internal:8088/proxy/application_1493976887575_0002/
17/05/05 05:46:13 INFO mapreduce.Job: Running job: job_1493976887575_0002
17/05/05 05:46:28 INFO mapreduce.Job: Job job_1493976887575_0002 running in uber mode : false
17/05/05 05:46:28 INFO mapreduce.Job:  map 0% reduce 0%
17/05/05 05:46:39 INFO mapreduce.Job:  map 17% reduce 0%
17/05/05 05:46:40 INFO mapreduce.Job:  map 33% reduce 0%
17/05/05 05:46:41 INFO mapreduce.Job:  map 50% reduce 0%
17/05/05 05:46:42 INFO mapreduce.Job:  map 67% reduce 0%
17/05/05 05:46:43 INFO mapreduce.Job:  map 83% reduce 0%
17/05/05 05:46:51 INFO mapreduce.Job:  map 100% reduce 0%
17/05/05 05:46:52 INFO mapreduce.Job:  map 100% reduce 100%
17/05/05 05:46:53 INFO mapreduce.Job: Job job_1493976887575_0002 completed successfully
17/05/05 05:46:53 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=69
                FILE: Number of bytes written=885581
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=1824
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=27
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=6
                Launched reduce tasks=1
                Data-local map tasks=6
                Total time spent by all maps in occupied slots (ms)=33213
                Total time spent by all reduces in occupied slots (ms)=5225
                Total time spent by all map tasks (ms)=33213
                Total time spent by all reduce tasks (ms)=5225
                Total vcore-seconds taken by all map tasks=33213
                Total vcore-seconds taken by all reduce tasks=5225
                Total megabyte-seconds taken by all map tasks=34010112
                Total megabyte-seconds taken by all reduce tasks=5350400
        Map-Reduce Framework
                Map input records=6
                Map output records=12
                Map output bytes=108
                Map output materialized bytes=204
                Input split bytes=1116
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=204
                Reduce input records=12
                Reduce output records=0
                Spilled Records=24
                Shuffled Maps =6
                Failed Shuffles=0
                Merged Map outputs=6
                GC time elapsed (ms)=198
                CPU time spent (ms)=4780
                Physical memory (bytes) snapshot=2962018304
                Virtual memory (bytes) snapshot=11123163136
                Total committed heap usage (bytes)=3281518592
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=708
        File Output Format Counters
                Bytes Written=97
Job Finished in 42.081 seconds
Estimated value of Pi is 3.15200000000000000000
```