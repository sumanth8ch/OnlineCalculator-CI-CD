In this project, Continous Integration(CI) is implemented using Git as well as CI/CD is also implemented using Jenkins.
The CI implementation using Git is done by writing the python-package.yml file which is in .github/workflows directory.
CI/CD pipeline is created based on the written Jenkinsfile which is implemented using the Jenkins server. 
Finally the application is deployed as a service on AWS Elastic BeanStalk.

This a flask-based online calculator based on REST API implemented by integrating different Microservices. 
It performs the microservices like: 
1)addition - add 
2)subtraction - sub 
3)multiplication - mul 
4)division - div 
The number of services can be added/removed and scaled up/down as per the requirement.

First run the main.py script on command line using: 
--------> python main.py 
Then it will present us with an url showing ip address and port on which the application is running. 
Copy that and paste in a web browser and usage should be as shown: 
------> url/Operation?A=?/B=? give us the result rounded upto 3 decimal places. 

For example to perform multiplication 
-------> http://127.0.0.1:5000/mul?A=2/5&B=3 

Note: If the input has some zero division error, the output will be none.
