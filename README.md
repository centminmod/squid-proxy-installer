# squid-proxy-installer

Forked version for [centminmod.com LEMP stack](http://centminmod.com) support. You can view differences between original and forked [here](https://github.com/hidden-refuge/squid-proxy-installer/compare/master...centminmod:master).

Squid Proxy Installer with Username-Password Authentication<br /><br /><br />
The Squid Proxy Installer (short: SPI) is a fully automated shell script to install an anonymous HTTP proxy based on Squid 3 with a username and password authentication through NCSA Auth and htpasswd. It requires no other input than your desired username and password. The default configuration listens on the default TCP port 3128!<br /><br />
SPI was written for the most common server Linux operating systems:
<ul>
<li>CentOS 5/6/7</li>
<li>Debian 6/7/8</li>
<li>Ubuntu (most versions are supported)</li>
<li>Fedora (most versions are supported)</li>
<li>More OS on request</li>
</ul>
64 Bit versions of some operating systems require more than 256 MB RAM for Squid to work (this includes generally Debian and Ubuntu as a outcome of various tests in OpenVZ).<br /><br /><br />
<b>How to use:</b><br /><br />
Step 1: Download the script to your server via wget/curl:<br />
<code>wget https://raw.githubusercontent.com/hidden-refuge/squid-proxy-installer/master/spi</code><br /><br />
Step 2: Give the file execution permissions with chmod:<br />
<code>chmod +x spi</code><br /><br />
Step 3: Run one of the following commands according to your OS:<br /><br />
CentOS 5:<br />
<code>./spi -rhel5</code><br /><br />
CentOS 6:<br />
<code>./spi -rhel6</code><br /><br />
CentOS 7:<br />
<code>./spi -rhel7</code><br /><br />
Debian 6 or 7:<br />
<code>./spi -debian</code><br /><br />
Debian 8:<br />
<code>./spi -jessie</code><br /><br />
Ubuntu:<br />
<code>./spi -ubuntu</code><br /><br />
Fedora:<br />
<code>./spi -fedora</code><br /><br />
Step 4: Remove the SPI file with rm:<br />
<code>rm -f spi</code><br /><br /><br />
<b>How to add more users:</b><br /><br />
You can easily add more users which are allowed to access your proxy with the command below:<br /><br />
Debain & Ubuntu:<br />
<code>htpasswd /etc/squid3/passwd username</code><br /><br />
CentOS/Fedora:<br />
<code>htpasswd /etc/squid/passwd username</code><br /><br />
Replace username with the actual username of the user you want to add.<br /><br /><br />
For help with Squid and in order to change the configuration according to your needs please consult the <a href="http://wiki.squid-cache.org/SquidFaq">Squid FAQ</a> and the <a href="http://wiki.squid-cache.org/">Squid wiki</a>.
