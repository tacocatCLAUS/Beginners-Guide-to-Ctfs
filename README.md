<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ile</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__html"><h1 id="a-beginners-guide-to-ctfs">A Beginners Guide To Ctf’s</h1>
<p><strong>picoCTF: The Webshell</strong><br>
To access the picoCTF webshell click webshell in the corner of the screen.<br>
<img src="https://i.imgur.com/nW8vxLJ.png" alt="Click This Button"><br>
Then you will see this screen:<br>
<img src="https://i.imgur.com/OmSxaGQ.png" alt="enter image description here"><br>
There are many different things you can do with this web terminal. (Linux)<br>
<a href="https://play.picoctf.org/practice/challenge/170">This Challenge</a> is a good example of using it. Here is the writeup for that:<br>
Question: Can you invoke help flags for a tool or binary?  <a href="https://mercury.picoctf.net/static/fc1d77192c544314efece5dd309092e3/warm">This program</a>  has extraordinarily helpful information…</p>
<p>Files: warm</p>
<p>Approach: After downloading the file running the command</p>
<blockquote>
<p>file warm</p>
</blockquote>
<p>shows it as an executable file.</p>
<p>When we try to run using</p>
<blockquote>
<p>./warm</p>
</blockquote>
<p>It gives error. One of the reason might be that it does not have execution permission. To give permission enter</p>
<blockquote>
<p>chmod +x warm</p>
</blockquote>
<p>running again gives</p>
<p>Hello user! Pass me a -h to learn what I can do!</p>
<p>Finally running</p>
<blockquote>
<p>./warm -h</p>
</blockquote>
<p>returns the flag</p>
<p>Flag: picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}</p>
<p>You can run file like this but to run Python (.py) you have to do something different.</p>
<p><strong>Python</strong></p>
<p>Python in the picoCTF terminal is preinstalled. To find out all commands do <code>$ man python</code>. This will list all commands. Here are the most helpful:</p>
<p><em>(Delete the brackets)</em><br>
<code>ls</code> Will list all files in your directory.<br>
<code>wget [url]</code> This will import your file into the terminal.<br>
<code>python [file]</code> Will run a file in your directory</p>
<blockquote>
<p><strong>A good example of these is <a href="https://play.picoctf.org/practice/challenge/166?page=1">this challenge.</a></strong></p>
<ul>
<li><code>python [file] -e [file.txt]</code> Will encrypt a file with the python script.</li>
<li><code>python [file] -d [file.txt]</code> Will decrypt a file with the python script.</li>
</ul>
</blockquote>
<ul>
<li><code>python [file]</code> Will run a python file.</li>
</ul>
<p>Here is an example of some of these commands:<br>
<img src="https://i.imgur.com/AWMV2EM.png" alt="enter image description here"></p>
<p><strong>Best programs on the terminal</strong></p>
<ol>
<li>Gobuster</li>
</ol>
<blockquote>
<p>Gobuster is a web exploitation program that searches for open ports. You can install it on mac with <a href="https://formulae.brew.sh/formula/gobuster">Homebrew</a>. Install it on linux</p>
</blockquote>
<ol start="3">
<li></li>
</ol>
<p><strong>Hacking: Web Exploitation/Osint</strong><br>
This is a guide to just hacking on the web in general.</p>
<p><strong>OWASP Top 10</strong><br>
The OWASP Top 10 are the most common vulnaribilities on a website in general. When doing ctf’s or just trying to hack a site remember to go by these 10 exploits.</p>
<ol>
<li>
<p>Injection: Imagine you have a password box on a website. Hackers can try to trick the website into executing harmful commands by injecting code through that box, like a secret language that only computers understand.</p>
</li>
<li>
<p>Broken Authentication: When websites have weak or easily guessable passwords or don’t protect your login information properly, hackers can easily break into your accounts.</p>
</li>
<li>
<p>Sensitive Data Exposure: Sometimes websites store sensitive information (like credit card numbers) insecurely. If a hacker gains access to that information, they can steal it and use it for illegal activities.</p>
</li>
<li>
<p>XML External Entities (XXE): This is when hackers trick a website into processing malicious XML files, allowing them to steal data or even take control of the entire server.</p>
</li>
<li>
<p>Broken Access Control: Websites sometimes have flaws in their access controls, allowing unauthorized users to access sensitive information or perform certain actions they shouldn’t be able to do.</p>
</li>
<li>
<p>Security Misconfigurations: This means when a website or application is not set up properly, making it easier for hackers to access sensitive information or exploit vulnerabilities.</p>
</li>
<li>
<p>Cross-Site Scripting (XSS): Hackers can inject malicious code into a website or application, making it execute this code on other users’ browsers. This could lead to stealing data or taking control of accounts.</p>
</li>
<li>
<p>Insecure Deserialization: When websites allow data to be deserialized (converted into another format), hackers can manipulate this process to execute malicious code or gain unauthorized access.</p>
</li>
<li>
<p>Using Components with Known Vulnerabilities: Many websites use third-party components or frameworks. If these components have known security vulnerabilities, hackers can exploit them to attack the website.</p>
</li>
<li>
<p>Insufficient Logging and Monitoring: If a website or application doesn’t log or keep track of important security events, it becomes difficult to detect and respond to any attacks or suspicious activities.</p>
</li>
</ol>
<p>These are the most common but there are more. There are many different exploits, many of which can be found on ctflearn or picoCTF.  Also make sure to observe and intercept the https requests and headers the website is doing. These can be very valuable.</p>
<p><strong>Https Rquesting &amp; Intercepting</strong><br>
Intercepting and editing headers can be a very valuable skill I clearly remember this episode of <em>Darknet Diaries</em> where this pen tester was looking at the https requests of a crate an account login page and one of the headers was <code>Admin=False</code> he changed it to true and became the admin. The best ways to intercept and send https requests are with <a href="https://chrome.google.com/webstore/detail/tamper-dev/mdemppnhjflbejfbnlddahjbpdbeejnn/related">Tamper Dev</a> and <a href="https://chrome.google.com/webstore/detail/talend-api-tester-free-ed/aejoelaoggembcahagimdiliamlcdmfm">Talend API Tester</a></p>
</div>
</body>

</html>
