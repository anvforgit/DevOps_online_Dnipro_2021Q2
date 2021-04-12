# Task 5.Part 1
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/448770922c1f025305709adf33385196d9208ca5/M5/screenshots_task%205/task5.1_1.png)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/448770922c1f025305709adf33385196d9208ca5/M5/screenshots_task%205/task5.1_2.png)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/448770922c1f025305709adf33385196d9208ca5/M5/screenshots_task%205/task5.1_3.png)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/448770922c1f025305709adf33385196d9208ca5/M5/screenshots_task%205/task5.1_4.png)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/448770922c1f025305709adf33385196d9208ca5/M5/screenshots_task%205/task5.1_5.png)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/448770922c1f025305709adf33385196d9208ca5/M5/screenshots_task%205/task5.1_6.png)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/448770922c1f025305709adf33385196d9208ca5/M5/screenshots_task%205/task5.1_7.png)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/448770922c1f025305709adf33385196d9208ca5/M5/screenshots_task%205/task5.1_8.png)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/448770922c1f025305709adf33385196d9208ca5/M5/screenshots_task%205/task5.1_9.jpg)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/448770922c1f025305709adf33385196d9208ca5/M5/screenshots_task%205/task5.1_10.jpg)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/448770922c1f025305709adf33385196d9208ca5/M5/screenshots_task%205/task5.1_11.jpg)


# Task 5.Part 2
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/6ca5d339d9263db75348b398706fc8fc86afc97b/M5/screenshots_task%205/task5.2_1.jpg)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/6ca5d339d9263db75348b398706fc8fc86afc97b/M5/screenshots_task%205/task5.2_2.jpg)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/6ca5d339d9263db75348b398706fc8fc86afc97b/M5/screenshots_task%205/task5.2_3.jpg)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/6ca5d339d9263db75348b398706fc8fc86afc97b/M5/screenshots_task%205/task5.2_4.jpg)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/6ca5d339d9263db75348b398706fc8fc86afc97b/M5/screenshots_task%205/task5.2_5.jpg)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/6ca5d339d9263db75348b398706fc8fc86afc97b/M5/screenshots_task%205/task5.2_6.jpg)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/6ca5d339d9263db75348b398706fc8fc86afc97b/M5/screenshots_task%205/task5.2_7.jpg)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/6ca5d339d9263db75348b398706fc8fc86afc97b/M5/screenshots_task%205/task5.2_8.jpg)
![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/6ca5d339d9263db75348b398706fc8fc86afc97b/M5/screenshots_task%205/task5.2_9.jpg)
## What are the types of devices and how to determine the type of device? Give examples.
 device types
Before we chat about how devices are managed, let's actually take a look at some devices.

$ ls -l /dev

brw-rw----   1 root disk      8,   0 Dec 20 20:13 sda

crw-rw-rw-   1 root root      1,   3 Dec 20 20:13 null

srw-rw-rw-   1 root root           0 Dec 20 20:13 log

prw-r--r--   1 root root           0 Dec 20 20:13 fdata

The columns are as follows from left to right:

Permissions
Owner
Group
Major Device Number
Minor Device Number
Timestamp
Device Name
Remember in the ls command you can see the type of file with the first bit on each line. Device files are denoted as the following:

c - character
b - block
p - pipe
s - socket
Character Device

These devices transfer data, but one a character at a time. You'll see a lot of pseudo devices (/dev/null) as character devices, these devices aren't really physically connected to the machine, but they allow the operating system greater functionality.

Block Device

These devices transfer data, but in large fixed-sized blocks. You'll most commonly see devices that utilize data blocks as block devices, such as harddrives, filesystems, etc.

Pipe Device

Named pipes allow two or more processes to communicate with each other, these are similar to character devices, but instead of having output sent to a device, it's sent to another process.

Socket Device

Socket devices facilitate communication between processes, similar to pipe devices but they can communicate with many processes at once.

Device Characterization

Devices are characterized using two numbers, major device number and minor device number. You can see these numbers in the above ls example, they are separated by a comma. For example, let's say a device had the device numbers: 8, 0:

The major device number represents the device driver that is used, in this case 8, which is often the major number for sd block devices. The minor number tells the kernel which unique device it is in this driver class, in this case 0 is used to represent the first device (a).

![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/6ca5d339d9263db75348b398706fc8fc86afc97b/M5/screenshots_task%205/task5.2_10.jpg)



![alt text](https://github.com/anvforgit/DevOps_online_Dnipro_2021Q2/blob/6ca5d339d9263db75348b398706fc8fc86afc97b/M5/screenshots_task%205/task5.2_11.jpg)

