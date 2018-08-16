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

- Knapsack-based AVR Task Demand Calculation Python3 implementation as found in Bijinemula et al.
- Digraph Real-Time task model demand calculations Python3 implementation as found in [_Refinement of Workload Models for Engine Controllers by State Space Partitioning_](http://user.it.uu.se/~yi/pdf-files/2017/ecrts17.pdf) by Mohaqeqi et al.
- Graphed comparison of above implementations using matplotlib

## Quickstart

### A) Open Virtual Appliance

1. Download and install [Oracle VirtualBox](https://www.virtualbox.org/wiki/Downloads).

2. Download the [Knapsack AVR Open Virtual Appliance (OVA)](https://waynestateprod-my.sharepoint.com/:f:/g/personal/ez9213_wayne_edu/Em0cgsbtXSRJs5vxJfcFpeAB-LUFyp5K6H0cxSClSs6Syg?e=NJsR2H).

3. Import the OVA by opening __VirtualBox__, selecting __File > Import Appliance__, and browsing to the _Knapsack-Based Approach Worst-Case AVR Demand.OVA_ file. Step-by-step import instructions can be found in Oracle's VirtualBox [documentation](https://docs.oracle.com/cd/E26217_01/E26796/html/qs-import-vm.html).

4. __Start__ the newly imported _Knapsack-Based Approach Worst-Case AVR Demand_ virtual machine.

5. _Open_ the _Efficient-Knapsack-for-AVR-tasks-RTSS2018_ folder on the _Desktop_.

6. __Right click the whitespace__ and select __Open in Terminal__.

7. __Enter__ `sudo ./simpleRunAll`

8. When prompted for a password, the password is: `RTSS2018`.

9. Wait Python3 to execute the demand calculations. A graph will be printed with similar results provided in the [publication](https://waynestateprod-my.sharepoint.com/:f:/g/personal/ez9213_wayne_edu/Em0cgsbtXSRJs5vxJfcFpeAB-LUFyp5K6H0cxSClSs6Syg?e=NJsR2H).

### B) Manual Install (Ubuntu 18.04)

1. Run the following shell script in linux terminal and enter the appropriate credentials when prompted:

    ```sh
    sudo apt-get update &&
    sudo apt-get install git python3 python3-pip && pip3 install -U numpy matplotlib
    ```

2. Clone the git repo:

    ```sh
    git clone https://github.com/bsk1410/Efficient-Knapsack-for-AVR-tasks-RTSS2018.git
    ```

3. Navigate to the git repo via terminal.

4. Run `sudo ./simpleRunAll` and enter the appropriate credentials when prompted.

5. Wait Python3 to execute the demand calculations. A graph will be printed with similar results provided in the [publication](https://waynestateprod-my.sharepoint.com/:f:/g/personal/ez9213_wayne_edu/Em0cgsbtXSRJs5vxJfcFpeAB-LUFyp5K6H0cxSClSs6Syg?e=NJsR2H).

## Getting Started

### Dependencies

| Link | Version Tested |
| ------ | ----------- |
| [Python3](https://www.python.org/) | 3.6.5 |
| [pip](https://pypi.org/project/pip/) | 9.0.1 |
| [NumPy](http://www.numpy.org/) | 1.13.3 |
| [matplotlib](https://matplotlib.org/api/pyplot_summary.html) | 2.2.3 |

### Tested System Specifications

| Property | Description |
| ------ | ----------- |
| OS | Ubuntu 18.04 LTS |
| Arch | 64-bit |
| CPU | Intel Core i7-6700 CPU @ 3.40 GHz x 8 |
| RAM | 8GB (7.7GB Available) |

### Selecting an Installation Method

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
| CPU | Intel Core i7-6700HQ CPU @ 2.60GHz __× 4__ |
| RAM | __8GB (7.8GB Available)__ |

</td></tr> </table>

### Guest Account Information

```sh
Login:      knapsackavr
Password:   RTSS2018
```

### Installing and Starting OVA

1. Download and install [Oracle VirtualBox](https://www.virtualbox.org/) from the VirtualBox [downloads page](https://www.virtualbox.org/wiki/Downloads).
2. Download the [Knapsack-Based Approach Worst-Case AVR Demand Open Virtual Appliance (OVA)](https://waynestateprod-my.sharepoint.com/:f:/g/personal/ez9213_wayne_edu/Em0cgsbtXSRJs5vxJfcFpeAB-LUFyp5K6H0cxSClSs6Syg?e=NJsR2H).
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

#### Step-By-Step Installation

Installing [git](https://git-scm.com/) [[1](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-14-04)]:

```sh
sudo apt-get install git
```

Installing [Python3](https://www.python.org/) [[2](https://askubuntu.com/questions/798123/how-do-i-install-python-3-5-2)]:

```sh
sudo apt-get update
sudo apt-get install python3
```

Installing [pip](https://pypi.org/project/pip/) [[3](https://askubuntu.com/questions/748929/no-module-named-numpy)]:

```sh
sudo apt-get install python-pip python3-pip
```

Installing [Tkinter](https://wiki.python.org/moin/TkInter) [[4](https://stackoverflow.com/questions/4783810/install-tkinter-for-python)]:

```sh
sudo apt-get install python3-tk
```

Installing [NumPy](http://www.numpy.org/) via pip [[3](https://askubuntu.com/questions/748929/no-module-named-numpy)]:

```sh
sudo pip3 install -U numpy
```

Installing [matplotlib](https://matplotlib.org/api/pyplot_summary.html) via pip [[5](https://matplotlib.org/users/installing.html)]:

```sh
sudo pip3 install -U matplotlib
```

Checking [Python3](https://www.python.org/) Version [[6](https://askubuntu.com/questions/505081/what-version-of-python-do-i-have)]:

```sh
python3 --version
```

Checking [NumPy](http://www.numpy.org/) Version in python3 [[7](https://stackoverflow.com/questions/1a520234/how-do-i-check-which-version-of-numpy-im-using)]:

```python3
>>>import numpy
>>>numpy.version.version
```

Checking [matplotlib](https://matplotlib.org/api/pyplot_summary.html) Version in python3 [[8](https://stackoverflow.com/questions/21473600/matplotlib-version)]:

```python3
>>>import matplotlib
>>>print('matplotlib: {}'.format(matplotlib.__version__))
```
[[1](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-14-04)] [https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-14-04](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-14-04)  
[[2](https://askubuntu.com/questions/798123/how-do-i-install-python-3-5-2)] [https://askubuntu.com/questions/798123/how-do-i-install-python-3-5-2](https://askubuntu.com/questions/798123/how-do-i-install-python-3-5-2)  
[[3](https://askubuntu.com/questions/748929/no-module-named-numpy)]  [https://askubuntu.com/questions/748929/no-module-named-numpy](https://askubuntu.com/questions/748929/no-module-named-numpy)  
[[4](https://stackoverflow.com/questions/4783810/install-tkinter-for-python)] [https://stackoverflow.com/questions/4783810/install-tkinter-for-python](https://stackoverflow.com/questions/4783810/install-tkinter-for-python)  
[[5](https://matplotlib.org/users/installing.html)] [https://matplotlib.org/users/installing.html](https://matplotlib.org/users/installing.html)  
[[6](https://askubuntu.com/questions/505081/what-version-of-python-do-i-have)] [https://askubuntu.com/questions/505081/what-version-of-python-do-i-have](https://askubuntu.com/questions/505081/what-version-of-python-do-i-have)  
[[7](https://stackoverflow.com/questions/1a520234/how-do-i-check-which-version-of-numpy-im-using)] [https://stackoverflow.com/questions/1a520234/how-do-i-check-which-version-of-numpy-im-using](https://stackoverflow.com/questions/1a520234/how-do-i-check-which-version-of-numpy-im-using)  
[[8](https://stackoverflow.com/questions/21473600/matplotlib-version)] [https://stackoverflow.com/questions/21473600/matplotlib-version](https://stackoverflow.com/questions/21473600/matplotlib-version)

#### Single-Script Installation

Combining the above step-by-step installation into a single command gives:

```sh
sudo apt-get update &&
sudo apt-get install git python3 python3-pip python3-tk && pip3 install -U numpy matplotlib
```

## Running Demand Analysis

Independent of which installation method was used to setup dependencies and the software, the following section details how to:

1. Configure Adaptive-Variable Rate demand profiles
2. Configuire Right Boundary Speed profiles
3. Execute a Knapsack-Based Demand Analysis
4. Execute a Digraph-Real-Time-Based Demand Analysis
5. Compare Knapsack-Based and Digraph-Real-Time-Based analysis to recreate publication data

### Configuration Editing

#### Adaptive Variable Rate (AVR) Demand Profiles

An Adaptive Variable Rate (AVR) Demand Profile specifies Worst-Case Execution Times (WCETs) for the speed ranges between right boundaries. To change the AVR Demand Profile, edit line 3 of `taskset.json`,

```json
"executionTimes": [965, 576, 424, 343, 277, 246],
```

and replace the default execution times with your own.

_Note: Custom execution times will be sorted in descending order. By default, non-decreasing order of execution times are not permitted._

#### Right Boundary Speed Profiles

A Right Boundary Speed profile specifies the speed ranges across which Worst-Case Execution Times (WCETs) are uniform. To change the Right Boundary Speed Profile, edit line 2 of `taskset.json`,

```json
"boundarySpeeds": [500, 1500, 2500, 3500, 4500, 5500, 6500],
```

and replace the default boundary speeds with your own.

_Note: Custom right boundary speed profiles __must have one less element__ than the AVR Demand profile._

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
