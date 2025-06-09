# Firewall-on-Windows
<h2>Enable UFW</h2>
<p>sudo ufw enable</p>
<h2>Check UFW Statut</h2>
<p>sudo ufw status verbose</p>
<h1>Allow Specific Traffic</h1>
<h2>Allow HTTP (port 80)</h2>
<p>sudo ufw allow 80/tcp</p>
<h2>Allow SSH (port 22)</h2>
<p>sudo ufw allow ssh</p>
<h2>Block all incoming traffic on port 23 (Telnet)</h2>
<p>sudo ufw deny 23</p>
<h2>Delete a Rule</h2>
<p>sudo ufw delete allow 80/tcp && sudo ufw delete allow ssh </p>
