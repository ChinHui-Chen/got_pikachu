# got_pikachu

# Run in docker

apt-get install git-all
cd /opt
git clone https://github.com/tensorflow/tensorflow

sudo apt-get install software-properties-common
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer

echo "deb [arch=amd64] http://storage.googleapis.com/bazel-apt stable jdk1.8" | sudo tee /etc/apt/sources.list.d/bazel.list
curl https://storage.googleapis.com/bazel-apt/doc/apt-key.pub.gpg | sudo apt-key add -

sudo apt-get update && sudo apt-get install bazel

cd /opt
touch WORKSPACE
cd tensorflow
./configure
sudo apt-get install swig
bazel build tensorflow/examples/image_retraining:retrain



mogrify -format jpg *.png



# Discussion

https://hackpad.com/2016-Got-Pikachu-zigftgEpMYU
