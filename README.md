[![Black Hat Arsenal](https://raw.githubusercontent.com/toolswatch/badges/master/arsenal/usa/2018.svg?sanitize=true)](http://www.toolswatch.org/2018/05/black-hat-arsenal-usa-2018-the-w0w-lineup/)

# Resilient-ML-Research-Platform 

This is a web platform to demo Machine Learning as a Service (MLaaS) on security researches. 
It has a machine learning (ML) pipeline to analyze data and also is a portal for backend user to emulate uploaded binaries.
It demos adversarial ML and countermeasures.

## Getting Started
### Dependancies
* CentOS or Ubuntu
* Apache Hadoop & Spark
* MongoDB
* Scikit-Learn, Numpy, Keras and related Python packages
* Django & SQLite
* Python 2.7
* Docker (optional)

### Installation
* Demo cluster by Docker containers - tiny bigdata platform on your Linux laptop:
```
docker login                    # Login to Docker Hub by your id & password
cd ./docker                     # cd to folder "docker" in git cloned project
chmod 755 *.sh                  # Change scripts to be executable
sudo ./setup_docker_linux.sh    # Create users on Linux and copy related files
./run_container_linux.sh        # Pull images from Docker Hub and run 4 containers:
                                #   HDFS/Spark master & slave1, mongo & Django web 
                                # Access at http://<your machine dns>:8000/ id=demo pwd=demo123
```
* For full installation, please follow the [Setup_Guide_CentOS7.pdf](Setup_Guide_CentOS7.pdf) 
  - Modify web configuation files for setting Hadoop/Spark/web/MongoDB hostnames
    * app.config
    * myml/settings.py
    * atdml/settings.py etc.

## Design Diagrams
### Data Flow:
<p align="center">
  <img src="../master/atdml/static/atdml/img/mlaas_arch_gpu.png" height="320">
</p>

### Software Stack:
<p align="center">
  <img src="../master/atdml/static/atdml/img/sw_stack.png" height="200">
</p>
Note: DNN worker to be released...

## Related Links

### <a href="../master/atdml/templates/atdml/about_mlaas.html" title="About MLaaS">About MLaaS</a>
### <a href="../master/atdml/templates/atdml/help_mlaas.html" title="RESTful API">Help for RESTful API</a>

## License
This project is licensed under the Apache 2.0 


