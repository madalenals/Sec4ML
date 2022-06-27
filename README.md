Sec4ML Tool 


Sec4ML is a tool to anonymize and preprocessing cybersecurity incidents datasets. Trough this tool is possible make cybersecurity incidents data public and reusable. The Sec4ML approach aims to apply in tabular datasets a set of anonymization and preprocessing algorithms for ML, as well as perform data triplication, making its publication feasible.

Sec4ML is capable of guiding the users in to anonymize and preprocessing data to generate datasets with its privacy preserved, in wich way of make then public and reusable.

Among the available functionalities, the operators for anonymization, as cryptography, noise adding e suppression. There are also operators for normalization, coding and handling of missing values, which are available according to the column(s) quantitative or qualitative data types over informed attributes.

Sec4ML supports reading from csv files and its output are: tripled data generated in format of N-Triple and the  dataset processed in csv format file.







Database connection configuration
All metadata about workflows executions are persisted in a stage database in SGBD PostgreSQL. The script to create this schema is in the file Sec4ML-shema.txt. 
The credentials to configure the database connections (native PostgreSQL) in the whole ETL (jobs, transformations and steps) is:

Name of connection: Sec4ML_Conn
hostname 		= localhost
database name 	= postgres
port number 	= 5432
username  	= postgres
password 		= event



PDI Configuration (Windows)

Installation of PDI 
Download from https://sourceforge.net/projects/pentaho/
Tutorial from
https://www.hitachivantara.com/en-us/pdf/white-paper/pentaho-community-edition-installation-guide-for-windows-whitepaper.pdf

Configuration of follow systems variables: 
JAVA_HOME = C:\Program Files\Java\jdk1.8.0_301
PENTAHO_DI_JAVA_OPTIONS = -Xmx1g (or bigger)
PENTAHO_JAVA = C:\Program Files\Java\jre1.8.0_301\bin\java.exe
PENTAHO_JAVA_HOME = C:\Program Files\Java\jre1.8.0_301

PDI Plugins (from Market Place)
- Cpython Script Executor
- PDI Encrypt Plugin
- Data sets and Units testes for PDI

PDI Plugin (from GitHub)
LinkedDataBR from
https://github.com/rogersmendonca/ETL4LOD




Python
Installation of fundamental libraries to Python Executor Step from https://help.pentaho.com/Documentation/9.0/Products/Python_Executor
- Pandas
Installation of Anaconda from https://repo.anaconda.com/archive/Anaconda3-2021.05-Windows-x86_64.exe.
Instructions of installation and use in https://pandas.pydata.org/getting_started.html.

- NumPy
Installation of NumPy from https://numpy.org/install/. Use PIP option with command:
> pip install numpy.

- Py4J
Installation of Py4J from https://www.py4j.org/download.html. Use PIP option with command:
> pip install py4j.

- Matplotlib 
Already part of Anaconda. However, could be installed from https://matplotlib.org/stable/users/installing.html.

- Scikit Learn

Installation of Scikit Learn from
https://scikit-learn.org/stable/install.html.
Use PIP option with command:  
pip install -U --user scikit-learn.

Package Crypto
Use PIP option with command:  
> pip install crypto

Package Pychryptodome

Install Visual Studio from
https://code.visualstudio.com/docs/?dv=win

Installation of Pychryptodome 
Use PIP option with command:
> pip install pycryptodomex --no-binary :all:
> python -m Cryptodome.SelfTest   (At the end must be  OK)

From documentation: 
https://www.pycryptodome.org/en/latest/src/installation.html#documentation




Execute the ETL
Start spoon.bat.
Open for CallSec4ML.kjb and start the job.








