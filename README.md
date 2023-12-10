# DS5111 Journal
# Computer ID: UPP2DH

This is the journal for the DS5111 class. The journal contains brief description about what we did in each module, what pop out for me as a new concept or code that I learned, exercises/labs completed and setbacks/holds I had to resolve to complete lab assignments. Anything I described in this journal is my openion or/and my understanding of the concepts we coverd in class. 

## Module 1: Git Fundamentals, Setting up github repository and AWS login 
In Module 1, we learned how to set up GIT repository and AWS. I was familiar with GIT repositories as I used it before in the program. Also, I have used AWS in one of the prior class. However, this is the first time I am doing EC2 instances. I very much enjoyed working and learning to create makefile and `vim`, `make` commands to execute codes. Also, working in Windows system is not straigthforward as in Mac OS as I have to use Pytty program to connect to EC2 instances.

## Module 2: Software Skills Part I
In Module 2, we learned more into working with EC2. I learned how to use assert to check conditions, start learning pytest and pylint. Also learned how to create a directory structure for testing. Though it took me a while to get everything running in the lab Software Skills I, I enjoyed very much working on it.

## Module 3: Software Skills Part II
In Module 3, we learned how to use Windows command promt to log into EC2 instance and use `Tmux`. I was successfully able to open Jupyter notebook in EC2 via the SSH and `Tmux`.

## Module 4: Software Skills Part III
In Module 4, we learned more about the the `Tmux` shell. I actually tested few `Tmux` shells using the previous lab and tested running simple python code. These attributes are very new to me as I always run Python either in my machine or online Jupyter notebook. I guess online version might be running in a `Tmux` type shell.

## Module 5: Software Testing
In Module 5, we dive more into testing skills. In the lab assignment, we try out few tests using `test_perceptron`. We tested passing and failing examples. This is very interesting for me as I never done these before in this setting. It took me a while to get the program working in lab. However, at the end, I was able successfully execute the taskes in the lab. 

## Module 6: CICD
In Module 6, we learned code automation. Learned about `YAML` and how to use `YAML` file to run tests within GitHub. There were lot more concepts covered in this module. However, I felt I did not grasp everything given not that much testing/exercises in labs related to this (at least not a comprehensive example to my understanding).

## Module 7: Create and Deploy Containers
In Module 7, we learned about containers. The difference between containers and virtual machines are bit suttle in my openion. However, as I understood, containers are sharing the same OS while virtual machine has its own OS inside OS. 

## Module 8: Database Design
In Module 8, we learned about database design. We learned about the difference between relational and non-relational databases, fundamentals in database objects, primary key, foreign key etc. I have learned databases in one of the previous classes in the program, so I am little bit familiar with it.

## Module 10: DBT - Module 12: DBT and Snowflake lab overview
In Module 10, we learned about DBT (Data Build Tool) and how to use it with Snowflake. We learned there is dbt package comes with Python that we can use instead of the web tool from DBT. We learned how to set up the dbt in EC2 virtual environment and create models from `seed` data. Here models are `.sql` files that create data tables for specific project using `seed` data. As I understood, `seed` data are the input/row data feeding into the project. Learned about `dbt_project.yml` and how its being used to configure and define the project. 

In Module 12, we learned more about connecting dbt with Snowflake. Professor walk us through every step of configuring dbt with Snowflake via an example. It was very helpful to understand the mechanics as well as start the lab. I was able to successfully configure dbt in EC2 virtual environment, connect it with Git and tested out few models. In the main lab, I was able to create table ,views, tests etc. This was very interesting module for me.

## Module 11: Overview of Snowflake and Docker lab
In Module 11, we learned more about Docker containers. We learned how to run a Docker in t2.large EC2 environment. Professor walk us through an example that demostrate how to configure Docker and run Docker commands using `makefile`. The lab was interesting, I had a hard time generating the image by running `make run` where it execute `docker run knn_iris`. When I go into the bash session inside the container, I see the printed outputs from `knn_iris.py` script, however I don't see the image `.png` if it creates. If I run `python knn_iris` inside the bash session in the container, it will run the `knn_iris.py` and create the `.png` file. This was strange and not sure whats hapening.  

## Some important codes to connect with EC2 and GIT repositories
### Connect to EC2 instance using Windows command prompt:
1. First need to get the Ubuntu subsystem running in Windows
    - Install WSL in command prompt
2. Once in Ubuntu shell, use `/mnt/c/Users/peuma/Downloads` to be in `Downloads` folder as once you create the EC2 `pem` key, it usually download into `Downloads` folder. `c/Users/peuma/Downloads` is the link to my `Downloads` folder.
3.  Now use the command
    `sudo ssh -i ds5111_docker.pem ubuntu@3.94.211.158` where `ds5111_docker.pem` is the `pem` key created for EC2 instance (that is in `Downloads` folder) and the ip address `3.94.211.158` is the public ip for the EC2 instance.

### Connect the EC2 instance with GIT repository:
1. Need to create a `SSH` key in EC2. The following command will create a public and private keys. Make sure to run the command in `.ssh/` folder. 
        -  `ssh-keygen -t rsa -b 4096 -C "e-mail address"`
2. It will prompt you to enter a name for the key and a password. Just press enter for both questions so `id_rsa` will be the name of the ssh key file and no password.
3. Now open `id_rsa.pub` that was created in step 1 using `vim id_rsa.pub` and copy the content. This content will be the key that is going to enter in Git hub.
4. In the Github, got to `Settings` and in `Settings` click on `SSH and GPG keys`. This will open a page that allows to enter the ssh key. Click on `New SSH key` button and enter the copied key in step 2.
5. Now we can clone the git repository by using `git clone ssh-link-to-repository`. Here you can get `ssh-link-to-repository` part in the command by clicking the down arrow on the button `<> Code` inside the repository. 

Overall, I really enjoyed the class, learned so many different concepts and gained lot more software skills. I think I need to do more examples/projects/labs to practice some of the concepts especially DBT-Snowflake related database work and Docker related work.




    

   

