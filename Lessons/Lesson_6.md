# Crontab:
A crontab file contains instructions to the cron daemon of the general form: "run this command at this time on this date". Each user can have their own crontab, and though these are files in /var directory, they are not intended to be edited directly.

## 1. Date format
[crontab.guru](https://crontab.guru/)

```
*    *    *   *    *  Command_to_execute
|    |    |    |   |       
|    |    |    |    Day of the Week ( 0 - 6 ) ( Sunday = 0 )
|    |    |    |
|    |    |    Month ( 1 - 12 )
|    |    |
|    |    Day of Month ( 1 - 31 )
|    |
|    Hour ( 0 - 23 )
|
Min ( 0 - 59 )
```



## 2. Specifying multiple values in a field
- The asterisk (```*```) operator specifies all possible values for a field. e.g. every hour or every day.

- The comma (```,```) operator specifies a list of values, for example: "1,3,4,7,8".

- The dash (```-```) operator specifies a range of values, for example: "1-6", which is equivalent to "1,2,3,4,5,6".

- The slash (```/```) operator, can be used to skip a given number of values. For example, "*/3" in the hour time field is equivalent to "0,3,6,9,12,15,18,21"; "*" specifies 'every hour' but the "/3" means that only the first, fourth, seventh...and such values given by "*" are used.


## 3. Crontab Options

|Code|Functionallity
|:---:|:---:|
|```crontab -e```|To Install or update job in crontab|
|```crontab -l```|To List Crontab entries|
|```crontab -r```|To Deinstall job from crontab|
|```crontab -i -r```|To Confirm Deinstall of job from crontab, use -i option|
|```crontab -s```|To add SELINUX security to crontab file, use -s option|
|```crontab -u username -e```|To edit other user crontab, user -u option and specify username|
|```crontab -u username -l```|To List other user crontab entries|