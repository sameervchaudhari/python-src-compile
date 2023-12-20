# python-src-compile
sudo apt-get update
sudo apt-get install -y build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev wget
wget https://www.python.org/ftp/python/3.12.1/Python-3.12.1.tgz

tar -xzf Python-3.12.1.tgz

rm Python-3.12.1.tgz
cd Python-3.12.1
./configure --enable-optimizations

htop
make -j4 #uses 4 cores. 
sudo make altinstall

/usr/local/bin/python3.12

vim ~/.bashrc
alias python="/usr/local/bin/python3.12"

source ~/.bashrc

python -m venv ~/.venv

source ~/.venv/bin/activate

touch requirements.txt

touch Makefile