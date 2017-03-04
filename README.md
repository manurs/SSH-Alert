# SSH-Alert (v1.6)
Get notified via email when somehting happend in the ssh (bad pass, user not allowed, reset server)

## dayReport.py
Report of the day

## alert.py
If something strange happend last hour you will recive an email

## Intructions

You have to create a aux.py like this:

```python
fromaddr = 'from@server.com'
toaddrs  = 'to@server.com'
pas = 'password of fromaddr'
```

### Create cron tasks:

- Open a terminal and write:

```
sudo crontab -e
```

- Select your text editor if is your fisrt time using cron

- Add this lines:

```
06 00 * * * python3 /route/dayReport.py
02 * * * * python3 /route/alert.py
```
