
# Set Time Automatically In Windows 10
How to force Windows 10 time to synch with a time serve?

![Languages](https://img.shields.io/github/languages/count/kakaa2993/Set-Time-Automatically-in-Win-10?color=%234d41c0)
![Top Language](https://img.shields.io/github/languages/top/kakaa2993/Set-Time-Automatically-in-Win-10?color=%234d41c0)
![Repository Size](https://img.shields.io/github/repo-size/kakaa2993/Set-Time-Automatically-in-Win-10?color=%234d41c0)
![Made By](https://img.shields.io/badge/made%20by-ZakaryaBelamiri-%234d41c0)

<br>

## What This Script Made For?
- This code was created by [Belamiri Zakarya](https://github.com/kakaa2993) to force Win 10 to sync the time with the time server in Windows 10 automatically without the user needing to do it manually.
- The script inspired from [this](https://answers.microsoft.com/en-us/windows/forum/all/how-to-force-windows-10-time-to-synch-with-a-time/20f3b546-af38-42fb-a2d0-d4df13cc8f43) question.
- Because in some machines that have Win 10 the time display isn't correct, so you need to change it every time you restart your PC with manual work.
- This script can fix the problem automatically with a click.

<br>

## The Requirement?
- This script needs only the connection to the internet to work!

<br>

## How To Use This Script?
- Just run the script ``as administrator``.

and voila! That is all that you need.

<be>

## Can I Use The Script Automatically?
You can make the script run automatically using ``Task Scheduler`` from Windows, here is a video showing you how you can use it manually [on YouTube](https://youtu.be/RSwOrK4m82U?si=PzW9tNA-4Gh97k0e).

Or you can also do it with ``cmd``:
- To create a task that runs a batch script "at log in" for any user and "as administrator" using the command line:
```batch
schtasks /create /tn "Name_of_Task" /sc onlogon /ru SYSTEM /rl HIGHEST /tr "C:\path\to\your\batch\sync_time_win.bat"
```

### PONTUS EDIT:
```
Sätt repeat interval till 1 hour indefinitely
```

Explanation of the command:

- `/sc onlogon`: the task should run when any user logs on.
- `/ru SYSTEM`: The task should run under the `SYSTEM` account, which has administrative privileges.
- `/rl HIGHEST`: Sets the privilege level to the highest available, effectively running the task as an administrator.
- `/tr "C:\path\to\your\batch\sync_time_win.bat"`: Specifies the path to the batch script that you want to run.

Replace `"Name_of_Task"` with the desired name for your task and `"C:\path\to\your\batch\sync_time_win.bat"` with the actual path to your batch script.

After running this command, the task will be created in Task Scheduler, and it will execute the specified batch script whenever any user logs on, running with administrative privileges.
Here's a table summarizing the available options for the `schtasks /create` command in Windows:

| Option           | Description                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| `/tn`            | Specifies the name of the task.                                                                              |
| `/sc`            | Specifies the schedule type (e.g., `ONLOGON`, `DAILY`, `WEEKLY`, `MONTHLY`, etc.).                           |
| `/ru`            | Specifies the user account to run the task under. Use `SYSTEM` for the highest privileges.                   |
| `/rl`            | Specifies the logon type (e.g., `HIGHEST`, `LIMITED`).                                                        |
| `/tr`            | Specifies the path to the program or script to be run by the task.                                           |
| `/st`            | Specifies the start time for the task (if applicable, based on the chosen schedule).                          |
| `/sd`            | Specifies the start date for the task.                                                                      |
| `/ed`            | Specifies the end date for the task.                                                                        |
| `/et`            | Specifies the end time for the task.                                                                        |
| `/mo`            | Specifies the modifier for recurrence (e.g., `1`, `2`, ..., `365`).                                          |
| `/i`             | Specifies the idle time to wait before running the task (only for `ONIDLE` trigger).                         |
| `/c`             | Specifies the comment for the task.                                                                         |
| `/f`             | Forces the creation of the task even if errors occur.                                                        |
| `/it`            | Sets the task to be interactive (must only be used with `/sc ONLOGON`).                                      |
| `/s`             | Specifies the remote server to connect to for creating the task.                                             |
| `/u`             | Specifies the user context under which the task should run.                                                  |
| `/p`             | Specifies the password for the user specified with `/u`.                                                     |
| `/triggers`      | Specifies one or more triggers for the task.                                                                |
| `/xml`           | Specifies the XML file containing the task definition.                                                       |

These are the main options for the `schtasks /create` command. You can combine them to customize the task according to your requirements.


<br>

Made by Belamiri Zakarya  :wave: [Get in touch!](https://github.com/kakaa2993)
