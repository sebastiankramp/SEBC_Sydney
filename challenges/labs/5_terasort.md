# Terasort as Cate

```bash
[cate@ip-172-31-11-170 ec2-user]$ hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/cate/tgen /user/cate/tsort640m
17/05/05 05:43:11 INFO terasort.TeraSort: starting
17/05/05 05:43:13 INFO hdfs.DFSClient: Created token for cate: HDFS_DELEGATION_TOKEN owner=cate@SEBASTIANKRAMP.AU, renewer=yarn, realUser=, issueDate=1493977393303, maxDate=1494582193303, sequenceNumber=1, masterKeyId=2 on 172.31.10.217:8020
17/05/05 05:43:13 INFO security.TokenCache: Got dt for hdfs://ip-172-31-10-217.eu-central-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.10.217:8020, Ident: (token for cate: HDFS_DELEGATION_TOKEN owner=cate@SEBASTIANKRAMP.AU, renewer=yarn, realUser=, issueDate=1493977393303, maxDate=1494582193303, sequenceNumber=1, masterKeyId=2)
17/05/05 05:43:13 INFO input.FileInputFormat: Total input paths to process : 2
Spent 443ms computing base-splits.
Spent 6ms computing TeraScheduler splits.
Computing input splits took 450ms
Sampling 10 splits of 392
Making 8 from 100000 sampled records
Computing parititions took 1005ms
Spent 1457ms computing partitions.
17/05/05 05:43:14 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-10-217.eu-central-1.compute.internal/172.31.10.217:8032
17/05/05 05:43:15 INFO mapreduce.JobSubmitter: number of splits:392
17/05/05 05:43:15 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1493976887575_0001
17/05/05 05:43:15 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.10.217:8020, Ident: (token for cate: HDFS_DELEGATION_TOKEN owner=cate@SEBASTIANKRAMP.AU, renewer=yarn, realUser=, issueDate=1493977393303, maxDate=1494582193303, sequenceNumber=1, masterKeyId=2)
17/05/05 05:43:16 INFO impl.YarnClientImpl: Submitted application application_1493976887575_0001
17/05/05 05:43:16 INFO mapreduce.Job: The url to track the job: http://ip-172-31-10-217.eu-central-1.compute.internal:8088/proxy/application_1493976887575_0001/
17/05/05 05:43:16 INFO mapreduce.Job: Running job: job_1493976887575_0001
17/05/05 05:43:25 INFO mapreduce.Job: Job job_1493976887575_0001 running in uber mode : false
17/05/05 05:43:25 INFO mapreduce.Job:  map 0% reduce 0%
17/05/05 05:43:36 INFO mapreduce.Job:  map 1% reduce 0%
17/05/05 05:43:38 INFO mapreduce.Job:  map 2% reduce 0%
17/05/05 05:43:44 INFO mapreduce.Job:  map 3% reduce 0%
17/05/05 05:43:46 INFO mapreduce.Job:  map 4% reduce 0%
17/05/05 05:43:52 INFO mapreduce.Job:  map 5% reduce 0%
17/05/05 05:43:53 INFO mapreduce.Job:  map 6% reduce 0%
17/05/05 05:43:59 INFO mapreduce.Job:  map 7% reduce 0%
17/05/05 05:44:01 INFO mapreduce.Job:  map 8% reduce 0%
17/05/05 05:44:06 INFO mapreduce.Job:  map 9% reduce 0%
17/05/05 05:44:07 INFO mapreduce.Job:  map 10% reduce 0%
17/05/05 05:44:13 INFO mapreduce.Job:  map 11% reduce 0%
17/05/05 05:44:16 INFO mapreduce.Job:  map 12% reduce 0%
17/05/05 05:44:20 INFO mapreduce.Job:  map 13% reduce 0%
17/05/05 05:44:21 INFO mapreduce.Job:  map 14% reduce 0%
17/05/05 05:44:27 INFO mapreduce.Job:  map 15% reduce 0%
17/05/05 05:44:29 INFO mapreduce.Job:  map 16% reduce 0%
17/05/05 05:44:35 INFO mapreduce.Job:  map 17% reduce 0%
17/05/05 05:44:37 INFO mapreduce.Job:  map 18% reduce 0%
17/05/05 05:44:42 INFO mapreduce.Job:  map 19% reduce 0%
17/05/05 05:44:47 INFO mapreduce.Job:  map 20% reduce 0%
17/05/05 05:44:49 INFO mapreduce.Job:  map 21% reduce 0%
17/05/05 05:44:53 INFO mapreduce.Job:  map 22% reduce 0%
17/05/05 05:44:56 INFO mapreduce.Job:  map 23% reduce 0%
17/05/05 05:45:02 INFO mapreduce.Job:  map 24% reduce 0%
17/05/05 05:45:03 INFO mapreduce.Job:  map 25% reduce 0%
17/05/05 05:45:07 INFO mapreduce.Job:  map 26% reduce 0%
17/05/05 05:45:09 INFO mapreduce.Job:  map 27% reduce 0%
17/05/05 05:45:15 INFO mapreduce.Job:  map 28% reduce 0%
17/05/05 05:45:17 INFO mapreduce.Job:  map 29% reduce 0%
17/05/05 05:45:24 INFO mapreduce.Job:  map 30% reduce 0%
17/05/05 05:45:25 INFO mapreduce.Job:  map 31% reduce 0%
17/05/05 05:45:30 INFO mapreduce.Job:  map 32% reduce 0%
17/05/05 05:45:33 INFO mapreduce.Job:  map 33% reduce 0%
17/05/05 05:45:37 INFO mapreduce.Job:  map 34% reduce 0%
17/05/05 05:45:40 INFO mapreduce.Job:  map 35% reduce 0%
17/05/05 05:45:44 INFO mapreduce.Job:  map 36% reduce 0%
17/05/05 05:45:49 INFO mapreduce.Job:  map 37% reduce 0%
17/05/05 05:45:51 INFO mapreduce.Job:  map 38% reduce 0%
17/05/05 05:45:54 INFO mapreduce.Job:  map 39% reduce 0%
17/05/05 05:45:59 INFO mapreduce.Job:  map 40% reduce 0%
17/05/05 05:46:02 INFO mapreduce.Job:  map 41% reduce 0%
17/05/05 05:46:06 INFO mapreduce.Job:  map 42% reduce 0%
17/05/05 05:46:09 INFO mapreduce.Job:  map 43% reduce 0%
17/05/05 05:46:13 INFO mapreduce.Job:  map 44% reduce 0%
17/05/05 05:46:19 INFO mapreduce.Job:  map 45% reduce 0%
17/05/05 05:46:20 INFO mapreduce.Job:  map 46% reduce 0%
17/05/05 05:46:26 INFO mapreduce.Job:  map 47% reduce 0%
17/05/05 05:46:29 INFO mapreduce.Job:  map 48% reduce 0%
17/05/05 05:46:34 INFO mapreduce.Job:  map 49% reduce 0%
17/05/05 05:46:41 INFO mapreduce.Job:  map 50% reduce 0%
17/05/05 05:46:47 INFO mapreduce.Job:  map 51% reduce 0%
17/05/05 05:46:52 INFO mapreduce.Job:  map 52% reduce 0%
17/05/05 05:46:57 INFO mapreduce.Job:  map 53% reduce 0%
17/05/05 05:47:01 INFO mapreduce.Job:  map 54% reduce 0%
17/05/05 05:47:04 INFO mapreduce.Job:  map 55% reduce 0%
17/05/05 05:47:09 INFO mapreduce.Job:  map 56% reduce 0%
17/05/05 05:47:12 INFO mapreduce.Job:  map 57% reduce 0%
17/05/05 05:47:16 INFO mapreduce.Job:  map 58% reduce 0%
17/05/05 05:47:19 INFO mapreduce.Job:  map 59% reduce 0%
17/05/05 05:47:24 INFO mapreduce.Job:  map 60% reduce 0%
17/05/05 05:47:28 INFO mapreduce.Job:  map 61% reduce 0%
17/05/05 05:47:30 INFO mapreduce.Job:  map 62% reduce 0%
17/05/05 05:47:33 INFO mapreduce.Job:  map 63% reduce 0%
17/05/05 05:47:37 INFO mapreduce.Job:  map 64% reduce 0%
17/05/05 05:47:40 INFO mapreduce.Job:  map 65% reduce 0%
17/05/05 05:47:44 INFO mapreduce.Job:  map 66% reduce 0%
17/05/05 05:47:47 INFO mapreduce.Job:  map 67% reduce 0%
17/05/05 05:47:52 INFO mapreduce.Job:  map 68% reduce 0%
17/05/05 05:47:56 INFO mapreduce.Job:  map 69% reduce 0%
17/05/05 05:48:00 INFO mapreduce.Job:  map 70% reduce 0%
17/05/05 05:48:02 INFO mapreduce.Job:  map 71% reduce 0%
17/05/05 05:48:08 INFO mapreduce.Job:  map 72% reduce 0%
17/05/05 05:48:13 INFO mapreduce.Job:  map 73% reduce 0%
17/05/05 05:48:15 INFO mapreduce.Job:  map 74% reduce 0%
17/05/05 05:48:20 INFO mapreduce.Job:  map 75% reduce 0%
17/05/05 05:48:22 INFO mapreduce.Job:  map 76% reduce 0%
17/05/05 05:48:27 INFO mapreduce.Job:  map 77% reduce 0%
17/05/05 05:48:28 INFO mapreduce.Job:  map 78% reduce 0%
17/05/05 05:48:33 INFO mapreduce.Job:  map 79% reduce 0%
17/05/05 05:48:35 INFO mapreduce.Job:  map 80% reduce 0%
17/05/05 05:48:40 INFO mapreduce.Job:  map 81% reduce 0%
17/05/05 05:48:43 INFO mapreduce.Job:  map 82% reduce 0%
17/05/05 05:48:49 INFO mapreduce.Job:  map 83% reduce 0%
17/05/05 05:48:56 INFO mapreduce.Job:  map 84% reduce 0%
17/05/05 05:48:57 INFO mapreduce.Job:  map 84% reduce 3%
17/05/05 05:48:59 INFO mapreduce.Job:  map 84% reduce 7%
17/05/05 05:49:01 INFO mapreduce.Job:  map 84% reduce 10%
17/05/05 05:49:03 INFO mapreduce.Job:  map 84% reduce 14%
17/05/05 05:49:04 INFO mapreduce.Job:  map 85% reduce 14%
17/05/05 05:49:11 INFO mapreduce.Job:  map 86% reduce 14%
17/05/05 05:49:20 INFO mapreduce.Job:  map 87% reduce 14%
17/05/05 05:49:25 INFO mapreduce.Job:  map 88% reduce 14%
17/05/05 05:49:26 INFO mapreduce.Job:  map 88% reduce 15%
17/05/05 05:49:31 INFO mapreduce.Job:  map 89% reduce 15%
17/05/05 05:49:37 INFO mapreduce.Job:  map 90% reduce 15%
17/05/05 05:49:45 INFO mapreduce.Job:  map 91% reduce 15%
17/05/05 05:49:51 INFO mapreduce.Job:  map 92% reduce 15%
17/05/05 05:49:57 INFO mapreduce.Job:  map 93% reduce 15%
17/05/05 05:50:06 INFO mapreduce.Job:  map 94% reduce 16%
17/05/05 05:50:12 INFO mapreduce.Job:  map 95% reduce 16%
17/05/05 05:50:18 INFO mapreduce.Job:  map 96% reduce 16%
17/05/05 05:50:26 INFO mapreduce.Job:  map 97% reduce 16%
17/05/05 05:50:32 INFO mapreduce.Job:  map 98% reduce 16%
17/05/05 05:50:38 INFO mapreduce.Job:  map 99% reduce 16%
17/05/05 05:50:46 INFO mapreduce.Job:  map 100% reduce 17%
17/05/05 05:50:48 INFO mapreduce.Job:  map 100% reduce 20%
17/05/05 05:50:50 INFO mapreduce.Job:  map 100% reduce 25%
17/05/05 05:50:52 INFO mapreduce.Job:  map 100% reduce 35%
17/05/05 05:50:54 INFO mapreduce.Job:  map 100% reduce 37%
17/05/05 05:50:56 INFO mapreduce.Job:  map 100% reduce 39%
17/05/05 05:50:58 INFO mapreduce.Job:  map 100% reduce 45%
17/05/05 05:50:59 INFO mapreduce.Job:  map 100% reduce 51%
17/05/05 05:51:00 INFO mapreduce.Job:  map 100% reduce 54%
17/05/05 05:51:01 INFO mapreduce.Job:  map 100% reduce 56%
17/05/05 05:51:03 INFO mapreduce.Job:  map 100% reduce 64%
17/05/05 05:51:04 INFO mapreduce.Job:  map 100% reduce 72%
17/05/05 05:51:05 INFO mapreduce.Job:  map 100% reduce 77%
17/05/05 05:51:08 INFO mapreduce.Job:  map 100% reduce 79%
17/05/05 05:51:09 INFO mapreduce.Job:  map 100% reduce 82%
17/05/05 05:51:10 INFO mapreduce.Job:  map 100% reduce 85%
17/05/05 05:51:11 INFO mapreduce.Job:  map 100% reduce 86%
17/05/05 05:51:12 INFO mapreduce.Job:  map 100% reduce 88%
17/05/05 05:51:15 INFO mapreduce.Job:  map 100% reduce 97%
17/05/05 05:51:21 INFO mapreduce.Job:  map 100% reduce 100%
17/05/05 05:51:22 INFO mapreduce.Job: Job job_1493976887575_0001 completed successfully
17/05/05 05:51:22 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=2906974017
                FILE: Number of bytes written=5800968873
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=6553659192
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=1200
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=392
                Launched reduce tasks=8
                Data-local map tasks=391
                Rack-local map tasks=1
                Total time spent by all maps in occupied slots (ms)=2096821
                Total time spent by all reduces in occupied slots (ms)=635050
                Total time spent by all map tasks (ms)=2096821
                Total time spent by all reduce tasks (ms)=635050
                Total vcore-seconds taken by all map tasks=2096821
                Total vcore-seconds taken by all reduce tasks=635050
                Total megabyte-seconds taken by all map tasks=2147144704
                Total megabyte-seconds taken by all reduce tasks=650291200
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Map output bytes=6684672000
                Map output materialized bytes=2843088150
                Input split bytes=59192
                Combine input records=0
                Combine output records=0
                Reduce input groups=65536000
                Reduce shuffle bytes=2843088150
                Reduce input records=65536000
                Reduce output records=65536000
                Spilled Records=131072000
                Shuffled Maps =3136
                Failed Shuffles=0
                Merged Map outputs=3136
                GC time elapsed (ms)=27094
                CPU time spent (ms)=1337480
                Physical memory (bytes) snapshot=190366871552
                Virtual memory (bytes) snapshot=634855469056
                Total committed heap usage (bytes)=224506937344
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=6553600000
        File Output Format Counters
                Bytes Written=6553600000
17/05/05 05:51:22 INFO terasort.TeraSort: done
```