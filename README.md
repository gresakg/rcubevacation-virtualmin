Vacation/AutoReply RoundCube plugin for Virtualmin
==================================================

[RoundCube Vacation](http://sourceforge.net/projects/rcubevacation/) plugin modified to work with Virtualmin and last RoundCube versions (Larry skin).

Installation
---------------

- install Roundcube using Virtualmin script intaller (e.g. into /home/mail.domain.com/public_html)

- clone this repository into plugins directory (/home/mail.domain.com/public_html/plugins) and rename it to "vacation"

- install squirrelmail\_vacation\_proxy:

  - cd vacation/extra/vacation_binary

  - edit config.mk and set WEBUSER to unix user which will run RoundCube (www-data if mod_php is used, mail.domain if FastCGI is used)

  - make

  - make install (as root)

- edit config/main.inc.php in RoundCube dir and set: $rcmail\_config['plugins'] = array('vacation');

- you should see tab Vacation in Settings now.
