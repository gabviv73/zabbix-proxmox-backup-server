# Detect failed or old backups

Use the API at (click the link):

https://pbshost.example.com:8007/api2/json/nodes/pubstor01/tasks?limit=3&typefilter=backup

It returns:
````
{
  "total": 4,
  "data": [
    {
      "upid": "UPID:pbshost:00000624:0000652A:000005B1:67106DB7:backup:PBSHOST\\x3avm-903:root@pam:",
      "node": "localhost",
      "pid": 1572,
      "pstart": 25898,
      "starttime": 1729129911,
      "worker_type": "backup",
      "worker_id": "PBSHOST:vm/903",
      "user": "root@pam",
      "endtime": 1729130021,
      "status": "OK"
    },
    {
      "upid": "UPID:pbshost:00000624:0000652A:000005AF:67106BA7:backup:PBSHOST\\x3avm-902:root@pam:",
      "node": "localhost",
      "pid": 1572,
      "pstart": 25898,
      "starttime": 1729129383,
      "worker_type": "backup",
      "worker_id": "PBSHOST:vm/902",
      "user": "root@pam",
      "endtime": 1729129908,
      "status": "OK"
    },
    {
      "upid": "UPID:pbshost:00000624:0000652A:000005AE:671069DA:backup:PBSHOST\\x3avm-803:root@pam:",
      "node": "localhost",
      "pid": 1572,
      "pstart": 25898,
      "starttime": 1729128922,
      "worker_type": "backup",
      "worker_id": "PBSHOST:vm/803",
      "user": "root@pam",
      "endtime": 1729129376,
      "status": "OK"
    }
  ]
}

````

So group by worker_id, the backup of the VM or HOST and check status and endtime.
