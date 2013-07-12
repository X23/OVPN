OVPN
====
Allows for the easy creation of streamlined ovpn files - ones where all certificates and keys are contained into one file. These are used where the separate files cannot be used for example OpenVPN on iOS.

The script automatically generates the file with UDP enabled as well as compression and all traffic to be tunnelled through.

<code>
 -h  show this help text
</code>
<code>
 -s  sets the location of the easy-rsa keys and certificates e.g. /etc/openvpn/easy-rsa/keys
</code>

Instructions;
<Ol>
<li>Download using <code> wget https://raw.github.com/X23/OVPN/master/ovpn-streamlined </code></li>
<li>Run <code>chmod +x ovpn-streamlined</code></li>
<li>Execute script for the first time using the<code> -s </code>to set the easy-rsa key path e.g. 
<code>./ovpn-streamlined -s /etc/openvpn/easy-rsa/keys </code> you only need to set this once</li>
<li>Now you can run the script to generate the file e.g. <code> ./ovpn-streamlined 10.1.1.1 1194 b </code> where 10.1.1.1 is the IP address of the server, 1194 is the port the server is on and a is the client name that the certificates are called. </li>

<b>It is necessary to run the script as root via login or sudo due to the permissions on the keys directory </b>
