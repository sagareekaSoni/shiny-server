# shiny-server

The purpose of the repository is to document task for setting up shiny server and rstudio server in local vm and deploying the application.


<b>OS :</b> CentOS 7

<b>Step 1 : </b> Intall EPEL

To install the necessary runtime dependencies for R, you will need to enable additional repositories for third-party or source packages

<i> yum install epel-release </i>

<a> https://docs.fedoraproject.org/en-US/epel/#_el7 </a>

<b>Step 2 : </b> Install R

 <i> sudo yum install R </i>

<a> https://www.rstudio.com/products/shiny/download-server/redhat-centos/ </a > 

<b>Step 3 : </b> Install  shiny

<i>
sudo su - \
-c "R -e \"install.packages('shiny', repos='https://cran.rstudio.com/')\"" </i>

<a> https://www.rstudio.com/products/shiny/download-server/redhat-centos/ </a> 

<b>Step 4 : </b> Install wget

Wget is a free software package for retrieving files using HTTP, HTTPS, FTP and FTPS, the most widely used Internet protocols.

<i> sudo yum install wget </i>

<b>Step 5 : </b> Install R studio

<i>
wget https://download2.rstudio.org/server/centos7/x86_64/rstudio-server-rhel-2021.09.2-382-x86_64.rpm
sudo yum install rstudio-server-rhel-2021.09.2-382-x86_64.rpm
</i>

<a> https://www.rstudio.com/products/rstudio/download-server/redhat-centos/ </a>  

<b>Step 6 : </b> Install Shiny Server

<i>
wget https://download3.rstudio.org/centos7/x86_64/shiny-server-1.5.17.973-x86_64.rpm
sudo yum install --nogpgcheck shiny-server-1.5.17.973-x86_64.rpm
</i>

<a> https://www.rstudio.com/products/shiny/download-server/redhat-centos/ </a> 

<b> Step 7 : </b> Created directory 

Created directory to save work for rstudio-server in /home/user/
<i> mkdir  shiny-app </i> 
i will use this folder to save work (shinyapp,rmarkdown,rscripts) in Rstudio 

<b> Step 8 </b> Log in R studio and set working directory then create app

default port number for Rstudio 8787

<b> Step 9 : </b> Install git

<i>
sudo yum install git
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
</i>

<b> Step 10 </b> Make git repository

Making /home/sagareeka/shiny-app/   as git repository  where we are saving the work 

First change working directory
<i> cd /home/sagareeka/shiny-app/ 
git init 
</i>

<b> Step 11 : </b> Create GitHub repository 

Go to GitHub and add a new repository and then copy the https address of GitHub

<b> Step 12 : </b> Push code to GitHub

<i>
git remote add origin https://github.com/____________.git
git add .
git commit -m "Initial commit"
git push -u origin master
</i>

<b> Step 13 : </b> Push code from git to shiny server to deploy the app

<i>
git clone https://github.com/____________.git
<i/>

<b> Step 14 : </b> Access Shiny app browser

ip:3838/shiny-apps/<folder where app.R file is saved>
<i>

