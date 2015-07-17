# Install oracle-jdk8
No other java
```
apt-get install -y wget openssl ca-certificates
cd /tmp
wget -qO jdk8.tar.gz --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u40-b25/jdk-8u40-linux-x64.tar.gz
sudo tar xzf jdk8.tar.gz -C /opt
sudo mv /opt/jdk* /opt/java
sudo update-alternatives --install /usr/bin/java java /opt/java/bin/java 100
sudo update-alternatives --install /usr/bin/javac javac /opt/java/bin/javac 100
```
Verification
```
$ java -version
java version "1.8.0_40"
Java(TM) SE Runtime Environment (build 1.8.0_40-b25)
Java HotSpot(TM) 64-Bit Server VM (build 25.40-b25, mixed mode)

$ javac -version
javac 1.8.0_40
```

# install lein
clojure general tool (lein) (dependencies, repl, runner...)
```
wget https://raw.githubusercontent.com/technomancy/leiningen/stable/bin/lein
sudo cp /lein /usr/local/bin/
sudo chmod a+x /usr/local/bin/lein
sudo apt-get install rlwrap
```

# install install clojurescript compiler
```
wget https://github.com/clojure/clojurescript/releases/download/r3308/cljs.jar
```

# create project (using figwheel)
[https://github.com/bhauman/figwheel-template](https://github.com/bhauman/figwheel-template)


## For basic project
```
lein new figwheel proy1
```
## For project using om
```
lein new figwheel proy1 -- --om # Adds a bare bones Om app, including Sablono.
```
## For project using reagent
```
lein new figwheel proy1 -- --reagent # Adds a bare bones Reagent app.
```

## development run
lein figwheel 


