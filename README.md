# Efficient-Knapsack-based-approach-for-AVR-task-Demand

The main code for the algorithm is in the file NewAlg.py.
DRTAlg.py contains the implementation of the DRT paper algorithm.
The outputs of the algorithms are in the txt files.
The file diffinFiles.py checks the difference in the outputs of our algorithm and the DRT algorithm.

The runtimes of the algorithms for randomly generated tasksets are in their respective folders.

To run any file: python3 <filename>
Optional Flags for files NewAlg.py and DRTAlg.py: -t <taskset_number>, -v (for verbose output)
choose one of [1,2,3] for taskset_number. Default 1.
1 - denotes the taskset-1 in Bijinemula et al.
2 - denotes taskset-2 in Bijinemula et al.
3 - to choose a custom taskset. Also, modify the taskset values in taskset.json file. Make sure to preserve the formatting in the file and that the number of boundary speeds is one more than the number of execution times and the magnitude of maximum acceleration and maximum deceleration should be the same.

## Features

- Knapsack-based AVR Task Demand Calculation
- Implementation of Digraph Real-Time task model demand calculations as found [_Refinement of Workload Models for Engine Controllers by State Space Partitioning_](http://user.it.uu.se/~yi/pdf-files/2017/ecrts17.pdf) by Mohaqeqi et al.

## Getting Started

### Dependencies

| Link | Version Tested |
| ------ | ----------- |
| [Python3](https://www.python.org/) | 3.6.5 |
| [pip](https://pypi.org/project/pip/) | 9.0.1 |
| [NumPy](http://www.numpy.org/) | 1.13.3 |

### Tested System Specifications

| Property | Description |
| ------ | ----------- |
| OS | Ubuntu 18.04 LTS |
| Arch | 64-bit |
| CPU | Intel Core i7-6700 CPU @ 3.40 GHz x 8 |
| RAM | 8GB (7.7GB Available) |

### Selecting an Installation Method:

__Option 1) Open Virtual Appliance (OVA) with Pre-Installed Dependencies.__  
Users may download an OVA with dependencies pre-installed and GitHub code / contents pre-downloaded.

__Option 2) De Novo Installation.__  
Users may install dependencies and download GitHub code / contents on their own system.

## Option 1) Open Virtual Appliance (OVA) with Pre-installed Dependencies

### OVA Specifications

<table>
    <tr><th>Host System</th><th>Guest System</th></tr>
    <tr><td>

| Property | Description |
| ------ | ----------- |
| OS | Ubuntu 18.04 LTS |
| Arch | 64-bit |
| CPU | Intel Core i7-6700HQ CPU @ 2.60GHz __× 8__ |
| RAM | __16GB (15.7GB Available)__ |

</td><td>

| Property | Description |
| ------ | ----------- |
| OS | Ubuntu 18.04 LTS |
| Arch | 64-bit |
| CPU | Intel Core i7-6700HQ CPU @ 2.60GHz __× 2__ |
| RAM | __4GB (3.9GB Available)__ |

</td></tr> </table>

### Guest Account Information

```sh
Login:      knapsackavr
Password:   RTSS2018
```

### Installing and Starting OVA

1. Download and install [Oracle VirtualBox](https://www.virtualbox.org/) from the VirtualBox [downloads page](https://www.virtualbox.org/wiki/Downloads).
2. Download [Knapsack-Based Approach Worst-Case AVR Demand.OVA](https://vt.edu/index.html), hosted by Virginia Tech.
3. Import the OVA by opening VirtualBox, selecting __File > Import Appliance__, and browsing to the _Knapsack-Based Approach Worst-Case AVR Demand.OVA_ file. Step-by-step import instructions can be found in Oracle's VirtualBox [documentation](https://docs.oracle.com/cd/E26217_01/E26796/html/qs-import-vm.html).
4. After importing, __Start__ the newly imported _Knapsack-Based Approach Worst-Case AVR Demand_.

## Option 2) Blank-Slate Dependencies

### System Specifications (_as used to generate test RTSS 2018 publication data_)

| Property | Description |
| ------ | ----------- |
| OS | Ubuntu 18.04 LTS |
| Arch | 64-bit |
| CPU | Intel Core i7-6700 CPU @ 3.40 GHz × 8 |
| RAM | 8GB (7.7GB Available) |

### Dependency Installation

Installing [Python3](https://www.python.org/) Ubuntu [[1](https://askubuntu.com/questions/798123/how-do-i-install-python-3-5-2)]:

```sh
sudo apt-get update
sudo apt-get install python3
```

Installing [pip](https://pypi.org/project/pip/) [[2](https://askubuntu.com/questions/748929/no-module-named-numpy)]:

```sh
sudo apt-get install python-pip python3-pip
```

Installing [NumPy](http://www.numpy.org/) via pip [[2](https://askubuntu.com/questions/748929/no-module-named-numpy)]:

```sh
sudo pip3 install -U numpy
```

Checking [Python3](https://www.python.org/) Version [[3](https://askubuntu.com/questions/505081/what-version-of-python-do-i-have)]:

```sh
python3 --version
```

Checking [NumPy](http://www.numpy.org/) Version [[4](https://stackoverflow.com/questions/1a520234/how-do-i-check-which-version-of-numpy-im-using)]:

```sh
python3
>>>import numpy
>>>numpy.version.version
```

[[1](https://askubuntu.com/questions/798123/how-do-i-install-python-3-5-2)] [https://askubuntu.com/questions/798123/how-do-i-install-python-3-5-2](https://askubuntu.com/questions/798123/how-do-i-install-python-3-5-2)  
[[2](https://askubuntu.com/questions/748929/no-module-named-numpy)]  [https://askubuntu.com/questions/748929/no-module-named-numpy](https://askubuntu.com/questions/748929/no-module-named-numpy)  
[[3](https://askubuntu.com/questions/505081/what-version-of-python-do-i-have)] [https://askubuntu.com/questions/505081/what-version-of-python-do-i-have](https://askubuntu.com/questions/505081/what-version-of-python-do-i-have)  
[[4](https://stackoverflow.com/questions/1a520234/how-do-i-check-which-version-of-numpy-im-using)] [https://stackoverflow.com/questions/1a520234/how-do-i-check-which-version-of-numpy-im-using](https://stackoverflow.com/questions/1a520234/how-do-i-check-which-version-of-numpy-im-using)

## Running Demand Analysis

Independent of which installation method was used to setup dependencies and the software, the following section details how to:

1. Configure Adaptive-Variable Rate demand profiles
2. Configuire Right Boundary Speed profiles
3. Execute a Knapsack-Based Demand Analysis
4. Execute a Digraph-Real-Time-Based Demand Analysis
5. Compare Knapsack-Based and Digraph-Real-Time-Based analysis to recreate publication data

### Configuration Editing

#### Adaptive Variable Rate (AVR) Demand Profiles

An Adaptive Variable Rate (AVR) Demand Profile specifies Worst-Case Execution Times (WCETs) for the speed ranges between right boundaries.

#### Right Boundary Speed Profiles

A Right Boundary Speed profile specifies the different speed range across which Worst-Case Execution Times (WCETs) are uniform.

### Executing Demand Analysis

#### Knapsack-Based Demand Analysis

#### Digraph-Real-Time-Based Demand Analysis

## Publication Information

### Research Publication

_An Efficient Knapsack-Based Approach for Calculating the Worst-Case Demand of AVR Tasks_ by Bijinemula et al. (Accepted)  
Real-Time Systems Symposium ([RTSS](http://2018.rtss.org/)) 2018 - Main Real-Time Track  
Nashville, Tennessee, USA

### Authors & Contact

| Author | Department | University | Location | Email |
| ------ | ---------- | ---------- | -------- | ----- |
| Sandeep Kumar Bijinemula | Electrical and Computer Engineering | [Virginia Tech](https://vt.edu/index.html) | Arlington, USA | bsk1410@vt.edu |
| Aaron Willcock | Computer Science | [Wayne State University](https://wayne.edu/) | Detroit, USA | aaron.willcock@wayne.edu |
| [Thidapat Chantem](https://ece.vt.edu/people/profile/chantem) | Electrical and Computer Engineering | [Virginia Tech](https://vt.edu/index.html) | Arlington, USA | tchantem@vt.edu |
| [Nathan Fisher](https://engineering.wayne.edu/profile/dx3281) | Computer Science | [Wayne State University](https://wayne.edu/) | Detroit, USA | fishern@wayne.edu |