# py_srvcli
# creating a simple service and client 

## first of all you need create a file for that you need to moove to the ros2_foxy source file, after that you can input the code that will create a file for cpp_srvcli


```
ros2 pkg create --build-type ament_python py_srvcli --dependencies rclpy example_interfaces
```
## The output has to be like this 
```
going to create a new package
package name: py_srvcli
destination directory: /home/beka/ros2_foxy/src
package format: 3
version: 0.0.0
description: TODO: Package description
maintainer: ['beka <bedboy383@gmail.com>']
licenses: ['TODO: License declaration']
build type: ament_python
dependencies: ['rclpy', 'example_interfaces']
creating folder ./py_srvcli
creating ./py_srvcli/package.xml
creating source folder
creating folder ./py_srvcli/py_srvcli
creating ./py_srvcli/setup.py
creating ./py_srvcli/setup.cfg
creating folder ./py_srvcli/resource
creating ./py_srvcli/resource/py_srvcli
creating ./py_srvcli/py_srvcli/__init__.py
creating folder ./py_srvcli/test
creating ./py_srvcli/test/test_copyright.py
creating ./py_srvcli/test/test_flake8.py
creating ./py_srvcli/test/test_pep257.py

[WARNING]: Unknown license 'TODO: License declaration'.  This has been set in the package.xml, but no LICENSE file has been created.
It is recommended to use one of the ament license identitifers:
Apache-2.0
BSL-1.0
BSD-2.0
BSD-2-Clause
BSD-3-Clause
GPL-3.0-only
LGPL-3.0-only
MIT
MIT-0

```

## After that you need to go the file that has been created and after that you need to create a new python file. To create a file you can use a "touch" function

```
touch server_member_function.py 
```
## and 
```
touch client_member_function.py
```
## After creating a file you need to coppy the code that has been given at the web-site.
## After copying the code you need to add an additional file that will run the ros2 functiomm and service function itself

```
colcon build --packages-select py_srvcli

```
##The output of this is following:

```
Starting >>> py_srvcli
--- stderr: py_srvcli                   
/usr/lib/python3/dist-packages/setuptools/command/install.py:34: SetuptoolsDeprecationWarning: setup.py install is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
---
Finished <<< py_srvcli [0.82s]

Summary: 1 package finished [1.00s]
  1 package had stderr output: py_srvcli
```
## Final step and to see that code is working you need to run the code that will show the main output
# at this step make sure that all the steps done as written in the example.

```
colcon build --packages-select py_srvcli

```
#The following function has to give a output like:

```
Starting >>> py_srvcli
--- stderr: py_srvcli                   
/usr/lib/python3/dist-packages/setuptools/command/install.py:34: SetuptoolsDeprecationWarning: setup.py install is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
---
Finished <<< py_srvcli [0.89s]

Summary: 1 package finished [1.05s]
  1 package had stderr output: py_srvcli
```
## For the next step you need to open another terminal
```
ros2 run py_srvcli service
```
## remark: Don't wait to see the output stright away after typing this code. To see the output it is necessary to open a new terminal.
```
ros2 run py_srvcli client 2 3
```
## When you see the following output:
```
[INFO] [1664878325.227472612] [minimal_client_async]: Result of add_two_ints: for 2 + 3 = 5
```
## open previous terminal to see the out put.
```
[INFO] [1664878325.216643058] [minimal_service]: Incoming request
a: 2 b: 3
```
# FINISH
