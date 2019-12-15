# MnTimeout
Javascript timeout checked by elapsed time

- Sample https://nakayama-muimu.github.io/mntimeout_example.html

On smartphone browsers, Javascript's setTimeout (and setInterval) method stops when the device sleeps.
If you want to force logout of web app when the user doesn't manipulate for a certain time, you cannot simply use setTimeout.
Instead, you need to check elapsed time since the last action of the user and judge whether the time exceeds the logout limit.

MnTimeout does this by using setInterval method in a short time (default is every one second) and checking periodically the time elapsed since the 'start' or 'renew'.
While the device sleeps, off course, we cannot check the elapsed time. But as soon as the device wakes up and the brower gets active, setInterval can work and check the elapsed time. In this way, you can ask the user, after a certain time, to do some action such as 'to log in again'.
