# Autonomous System Number  Lookupby IP  Address (BASH Script)
![ASLOOKUP](https://raw.githubusercontent.com/mnbarinov/as_number_lookup_by_ip/main/aslookup.png)<br />
Autonomous System Number  Lookup by IP  Address

<h2>Dependencies</h2>
<ol>
  <li><h3>Whois</h3>
    <code>sudo apt -y install whois</code>    
  </li>
</ol>
<h2>Create and Install</h2>
<ol>
  <li>
<p>
Create bash script:<br />
<code>nano aslookup.sh</code>
</p>
 </li>
 <li>
<p>
Insert code<br />
<code>
#!/bin/bash
</code><br />
<code>
whois -h whois.cymru.com -v $1
</code>
</p>
</li>
<li>
  <p>
    Save<br />
    <code>ctrl+o ENTER</code>
  </p>
</li>
<li>
  <p>
  Change the access permissions<br />
    <code>
      sudo chmod +x aslookup.sh
    </code>
  </p>
</li>
<li>
  <p>Installation<br />
    <code>
      cp aslookup.sh /usr/bin/aslookup
    </code>
  </p>
</li>
</ol>
  
<h2>How to use</h2>
<p>
  <b>Command:</b><br />
<code>aslookup 8.8.8.8</code></p>
<p><b>Result:</b><br />
<pre>
<code>
AS      | IP               | BGP Prefix          | CC | Registry | Allocated  | AS Name
15169   | 8.8.8.8          | 8.8.8.0/24          | US | arin     | 1992-12-01 | GOOGLE, US
</code>
</pre>
</p>
