# SeleniumWithCucumber
This is an sample project to demonstrate how to work with Selenium and cucumber for Java

## More Information
The complete code base development video is available in ExecuteAutomation YouTube channel 
https://www.youtube.com/playlist?list=PL6tu16kXT9Pqr70SZlwcmTSAfOw_0Qj3R


## Cucumber BDD video Series (YouTube)
https://www.youtube.com/playlist?list=PL6tu16kXT9PpteusHGISu_lHcV6MbBtA6

## Cucumber BDD video Series (Udemy)
https://www.udemy.com/cucumber-with-selenium/

### For more articles and videos
Visit http://www.executeautomation.com

# sample Chrome Driver information
https://christopher.su/2015/selenium-chromedriver-ubuntu/

Installing Selenium and ChromeDriver on Ubuntu
I recently got Selenium, Google Chrome, and ChromeDriver installed and working on a VM running 64-bit Ubuntu 14.04. Here’s how:

First, install Google Chrome for Debian/Ubuntu:

sudo apt-get install libxss1 libappindicator1 libindicator7
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb

sudo dpkg -i google-chrome*.deb
sudo apt-get install -f
Now, let’s install xvfb so we can run Chrome headlessly:

sudo apt-get install xvfb
Install ChromeDriver:1

sudo apt-get install unzip

wget -N http://chromedriver.storage.googleapis.com/2.26/chromedriver_linux64.zip
unzip chromedriver_linux64.zip
chmod +x chromedriver

sudo mv -f chromedriver /usr/local/share/chromedriver
sudo ln -s /usr/local/share/chromedriver /usr/local/bin/chromedriver
sudo ln -s /usr/local/share/chromedriver /usr/bin/chromedriver
Install some Python dependencies and Selenium:

# Install pip:
sudo apt-get install python-pip

## (Optional) Create and enter a virtual environment:
# sudo apt-get install python-virtualenv
# virtualenv env
# source env/bin/activate

# Install Selenium and pyvirtualdisplay:
pip install pyvirtualdisplay selenium
Now, we can do stuff like this with Selenium in Python:

from pyvirtualdisplay import Display
from selenium import webdriver

display = Display(visible=0, size=(800, 600))
display.start()
driver = webdriver.Chrome()
driver.get('http://christopher.su')
print driver.title
Footnotes
1: You can find all the ChromeDriver releases here. If you’re using a 32-bit system or a non-Linux OS, the ChromeDriver download used above won’t work.


