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

<h1>How a Firewall Filters Traffic</h1>

  <h2>Basic Filtering Methods:</h2>
  <ul>
    <li><strong>By IP Address:</strong> Block or allow based on source/destination IP.</li>
    <li><strong>By Port:</strong> Control traffic using TCP/UDP port numbers.</li>
    <li><strong>By Protocol:</strong> Filter by protocol (TCP, UDP, ICMP, etc.).</li>
    <li><strong>By Application:</strong> Identify and control traffic based on application.</li>
    <li><strong>By Direction:</strong> Apply rules to inbound or outbound traffic.</li>
    <li><strong>By State:</strong> Track connection state (e.g., new, established).</li>
  </ul>

  <h2>Types of Firewalls:</h2>
  <table>
    <thead>
      <tr>
        <th>Type</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Packet Filtering</td>
        <td>Inspects headers of packets (IP, port, protocol).</td>
      </tr>
      <tr>
        <td>Stateful Inspection</td>
        <td>Tracks connection states to allow/deny packets.</td>
      </tr>
      <tr>
        <td>Application Layer</td>
        <td>Inspects application data (e.g., HTTP, FTP).</td>
      </tr>
      <tr>
        <td>Next-Gen Firewall</td>
        <td>Combines all features plus app and threat intelligence.</td>
      </tr>
    </tbody>
  </table>

  <h2>Example Rule:</h2>
  <p><code>Allow TCP from any IP to 192.168.1.5 on port 22 (SSH)</code></p>
  <p>This rule permits only SSH traffic to the server; all other ports remain blocked.</p>
