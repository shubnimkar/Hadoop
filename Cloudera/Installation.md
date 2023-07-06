Installation of Cloudera - CDP [Cloud Data Platform] single node cluster on linux machines (RHEL/Centos)

### Step 1:
  * Disable SELINUX
 
        setenforce 0
    
  * Disable firewalld

        systemctl stop firewalld
        systemctl stop firewalld

        
![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/d1a46624-91c1-47d5-a1ad-792e24ba521a)


* Add hostname and IP of machine in /etc/hosts file.

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/dadf929f-58f9-42f6-85e1-fc04b13bd433)


### Step 2:

* Now run the following commands for the cluster installation

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/3bc38694-6645-4c96-bab9-07c77585116b)


    wget https://archive.cloudera.com/cm7/7.4.4/cloudera-manager-installer.bin
    chmod u+x cloudera-manager-installer.bin
    sudo ./cloudera-manager-installer.bin
   
We can get above commands from online cloudera website to install CDP

Link is mentioned below:

[Cloudera CGP](https://www.cloudera.com/downloads/cdp-private-cloud-trial/cdp-private-cloud-base-trial.html)

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/501b830b-3a2a-42aa-a046-5dfce2f3727d)

Now proceed with the dialog box for the installation:

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/6806c3a6-55c3-46cf-a5b2-ec6ab7720de2)

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/027133f2-7b5e-493a-a338-f1a3daffd802)

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/b3c31022-dba9-4a46-a30a-2a606496f94c)

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/dc466bc5-4386-4f29-9c8a-a01053861da7)

Here you can see the installation has begun and it will present with some instruction to access the web UI so that we can move forward with the cluster deployment. 
The dialog box you can see in the next image;

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/e0845a77-6fc4-46ea-8427-c4913d4a4545)


### Step 3:

This is the web portal you can login here with
http://localhost:7180
and default login ID and password is “admin”


![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/df6c31d3-6572-48df-8bb1-ad20fb0d8ca3)


Select try cloudera data platform for 60 days

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/26c3a5b9-be64-4cd9-8ae1-fd7b20e43e11)
Continue

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/c70045c4-59e3-4ca9-8116-7c53700ca171)

Name your cluster and comtinue

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/6a5d8d7a-f398-40a6-a6d4-bbbf404fe306)

Mention the hostname for the hosts to be added in the cluster and it’ll scan for it and continue

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/96948e90-ee95-42ce-bb41-1fd2e9365297)

Select default settings and next

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/0f8a2d09-22d8-4cfc-9879-0b9b26cdec56)

Select version of JDK as per needed

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/926f14b5-47dc-405b-9ab7-f47cadd291ae)

Mention the password for the machines where the installations are taking place

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/24efe370-c86b-4f46-9409-28fe203d3f27)

And it’ll start

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/389f1ce8-f9ae-4763-a3bf-fcd1a7ea452b)

It’ll download the packages and install and distribute them amongst nodes

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/41561adf-579a-480e-b33d-ed8d5cdfa72b)

Check for the performances and select I understand risks ,sometimes error will occur but we can figure it out later


![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/be9f08bf-5f1c-49a4-b241-237c1cd9fce6)

Now Select Services which you want to install in cluster

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/f96ed883-469e-400c-92eb-4cecf54cae49)

Here I’ve taken HDFS, HIVE, HIVE on TEZ ,spark, tez,YARN,YARN manager, zookeeper

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/5f312652-5cb5-4505-980e-97dcd849e796)


![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/236ae4e3-2c95-4716-b08f-c13b728ae341)

Assign Roles

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/d1c6e4df-27eb-407e-a731-fd06d9e69b50)

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/e144f9b4-aceb-49a6-99e0-74a7ccf078a4)

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/d6d5219a-a8b6-4912-88e4-40b33ff40e38)

These are default passwords for data bases please keep handy or you can go with custom too

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/cf6e4d2e-37b1-44c9-a2e6-6358ac6ec882)

Select continue


![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/b46f0598-2bfc-4d84-958c-4d909337185d)

If you wan to change some configuration you can do it here or else later too

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/a4824100-b5a8-4b5c-ac00-e5c789781c28)

Continue

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/3d10f8f6-3ff8-42b6-aab2-eb30affaf894)

Finish

![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/ae9ab90b-1f91-4e55-9a76-d78520d819de)


![image](https://github.com/shubnimkar/Cloudera-hadoop/assets/46809421/0f6b61fe-2770-4eaa-b57a-f236fd3f6b1a)

Here is our cluster up and ready
