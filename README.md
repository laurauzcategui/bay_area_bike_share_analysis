# bay_area_bike_share_analysis
Bay_Area_Bike_Share_Analysis project for Data Analyst Nanodegree

This is the first project for the Data Analyst Nanodegree program @ Udacity. 

This project is meant to provide a quick opportunity to experience the submission process and feedback for learning and getting familiar with the tools. 

As I was working sometimes from different environments, I decided to simplify the work by using Docker :) without the need to install and work through dependencies. 

Here the steps I used in order to have a docker image with Anaconda running: 

```bash
$ docker pull continuumio/anaconda
# check it's working 
$ docker run -i -t continuumio/anaconda /bin/bash
# exit 
$ exit

# Let's open the Jupyter notebook 
$ docker run -i -t -p 8888:8888 continuumio/anaconda /bin/bash -c "/opt/conda/bin/conda install jupyter -y --quiet && mkdir /opt/notebooks && /opt/conda/bin/jupyter notebook --notebook-dir=/opt/notebooks --ip='*' --port=8888 --no-browser --allow-root"

# It should give you a message like 
# Copy/paste this URL into your browser when you connect for the first time,
#    to login with a token:
#        http://localhost:8888/?token=[TOKEN]
 
 
# Let's check the name of your image running  
$ docker ps 
# Take the name from the output (last column usually)  and enter to the container 
# CONTAINER ID  IMAGE   COMMAND   CREATED             STATUS              PORTS                    NAMES
# eebfa7197e5b        continuumio/anaconda   "/usr/bin/tini -- ..."   4 hours ago         Up 4 hours          0.0.0.0:8888->8888/tcp   flamboyant_banach
$ docker exec -it flamboyant_banach bash
# adquire the code for starting either with wget ( Start point ) or git clone of your repo. 
$ wget https://d17h27t6h515a5.cloudfront.net/topher/2017/July/597a2811_dandp0-bikeshareanalysis/dandp0-bikeshareanalysis.zip
# install unzip 
$ apt-get install unzip
# Extract the content under the notebook
$ unzip dandp0-bikeshareanalysis.zip -d /opt/notebooks

# If you are cloning from your repo, do the git clone and from your local repo copy the notebook to the location where all 
# notebooks are.
$ cp Bay_Area_Bike_Share_Analysis.ipynb /opt/notebooks/

```

Finally work on your Analysis and after you are done just git commit your work and you are done! 


If you have any questions or suggestions, feel free to reach out by opening an issue or send a PR :) 

Good Luck.

@laurauzcategui
