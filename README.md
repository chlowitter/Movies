// set up instance using us-east-1 as region
//Install java
http://aws-labs.com/ubuntu-install-java-8/
sudo add-apt-repository -y ppa:webupd8team/java
sudo apt-get update
echo debconf shared/accepted-oracle-license-v1-1 select true | sudo debconf-set-selections
echo debconf shared/accepted-oracle-license-v1-1 seen true | sudo debconf-set-selections
sudo apt-get -y install oracle-java8-installer java -version

//Download dynamodb- Use US West (should be ok, was working for me earlier)
wget http://docs.aws.amazon.com/amazondynamodb/latest/gettingstartedguide/GettingStarted.Download.html
tar  xfz   ~/dynamodb_local_latest.tar.gz
java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar -sharedDb -inMemory

//download php
sudo apt-get install php
curl -sS https://getcomposer.org/installer | php
php composer.phar require aws/aws-sdk-php	

//go to link and follow directions to download data for the movies database:
//http://docs.aws.amazon.com/amazondynamodb/latest/gettingstartedguide/GettingStarted.PHP.02.html

//use php code files to create, insert data, and query dynamodb
