# How to install course tools

## **Needed Tools**

**List of tools:**

* **Slack**
* **Zoom**
* **VS Code**
* **Chrome**
* **GIT**
* **Node**
* **PostgreSQL**
* **Dbeaver**

## Install software in Ubuntu

You can use the **Ubuntu Software Center** to search and install new software packages in the computer, it is like the Play Store used in Android mobiles. You will find this icon in the left bar:\
****

![](https://lh3.googleusercontent.com/wknLkHZfEMeuvEAmyipFT5DL9vw\_mnL6DImuQw968FmehaMG6xP-3RmLeKB3ake\_VLo3s42l-BFZ0hmL4P0I73tT5OnyXPfcCDU97cSeesMF4ba0-rr2OAN-aGF\_jHxJz71C7-mC)

## **Slack**

**Ubuntu**: Go to the Ubuntu Software Center, search and install it.

**Others:** Go to the [Slack Website](https://slack.com/intl/es-es/download) and follow the instructions.

## **Visual Studio Code**

**Ubuntu**: Go to the Ubuntu Software Center, search and install it.

**Others:** Go to the [Visual Studio Code Website](https://code.visualstudio.com/download) and follow the instructions.

## **Node**

Ubuntu: Go to the Ubuntu Software Center, search and install it.

Go to the [NodeJS Website](https://nodejs.org/es/download/) and follow the instructions.\


To check installation open a Terminal and execute:

```
node -v
```

## **Git**

**Ubuntu**: Go to the Ubuntu Software Center, search and install it.

**Others**: Go to the Git Website and follow the instructions.

To check installation open a Terminal and execute

```
git
```

## **Chrome**

**Ubuntu**: open the terminal and execute the following commands

```
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
```

```
sudo apt install ./google-chrome-stable_current_amd64.deb
```

**Others**: Go to [Chrome Website](https://www.google.com/chrome/browser/desktop/index.html) and follow the instructions

## **PostgreSQL**

#### **Ubuntu:**&#x20;

open the terminal and execute the following commands

sudo apt-get install postgresql-12

On Linux systems, there is no default password set.

To set the default password:

Run the psql command from the postgres user account:

```
sudo -u postgres psql postgres
```

Set the password, try to use the same password you have in your computer, migracode

```
\password postgres
```

Enter the password.

And finally close psql with the command:

```
\q
```

More info in: [https://docs.boundlessgeo.com/suite/1.1.1/dataadmin/pgGettingStarted/firstconnect.html](https://docs.boundlessgeo.com/suite/1.1.1/dataadmin/pgGettingStarted/firstconnect.html) \


**Others**: https://www.postgresql.org/download/\
