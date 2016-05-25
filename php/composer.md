#1.env require 
1.php version > 5.5.9

2.vpn allow connect foreign internet
#2.install composer 

	php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
	php -r "if (hash_file('SHA384', 'composer-setup.php') === '92102166af5abdb03f49ce52a40591073a7b859a86e8ff13338cf7db58a19f7844fbc0bb79b2773bf30791e935dbd938') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
	php composer-setup.php
	php -r "unlink('composer-setup.php');"

#3.change env
1.mv composer.phar /usr/local/bin/composer

2.sudo chown qiaolx.qiaolx /home/qiaolx/.composer/cache -R

#4.install composer repo
composer require "laravel/installer"

