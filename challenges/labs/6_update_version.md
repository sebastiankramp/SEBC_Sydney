# Version

## before update
```bash
[root@ip-172-31-15-167 krb5kdc]# curl -u 'admin:sydney' "http://localhost:7180/api/v14/cm/version"
{
  "version" : "5.10.1",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170319-2001",
  "gitHash" : "f226435f6fa5f545543c00245900ae43bea7a29c",
  "snapshot" : false
}
```

## after update
```bash
[root@ip-172-31-15-167 krb5kdc]# curl -u 'admin:sydney' "http://localhost:7180/api/v14/cm/version"
{
  "version" : "5.11.0",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170412-1255",
  "gitHash" : "70cb1442626406432a6e7af5bdf206a384ca3f98",
  "snapshot" : false
}
```