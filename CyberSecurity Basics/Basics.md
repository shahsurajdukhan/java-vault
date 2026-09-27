## What is CyberSecurity?
	Cybersecurity is the practice of protecting
			- Computers
			- Networks
			- Devices
			- Data
			- Cloud Systems
			- Users and identities
			- Organizations
		from unauthorized access,attacks,damage,or disruptions.


## CIA Triad
	 C = Confidentiality > only authorized people can access
	 I = Integrity > Data should not be changed without authorization
	 A = Availability > Systems and data should be available when authorized users need them
	 
	this is the most important basic concept in cybersecurity.

### Remember:

```
Confidentiality → Nobody unauthorized can SEE it

Integrity       → Nobody unauthorized can CHANGE it

Availability    → Authorized users can USE it
```

This will appear everywhere in cybersecurity.


## Imp Terms : Asset, Threat, Vulnerability, Risk

	Asset > something valuable that needs protection.
	for ex: customer database, source code, credit card information

	Threat > something that could cause harm
	for ex: hacker,malware,insider,phishing,natural disaster

	Vulnerability > a weakness that can be exploited
	for ex: weak password is a vulnerability

	Risk > the possibility that a threat will exploit a vulnerability and cause damage

### Example

```
Asset:
Company database

Threat:
Attacker

Vulnerability:
SQL Injection

Risk:
Attacker steals customer data
```


## Authentication & Authorization

		Authentication means who are you?
		common authentication methods
		- Password
		- OTP
		- fingerprint
		- face recognition
		- security key

		Authorization means what are you allowed to do?
		- Student > can view marks > cannot modify marks
		- Teacher > can view marks > can modify marks

## Encryption & Hashing

		Encryption means readable data is converted into unreadable data
		Plaintext > Encryption > Ciphertext
		Hello > Encryption > x7@p91
		Encryption is generally reversible using the appropriate key
		Encryption is used for :
		- HTTPS
		- Secure Messaging
		- Disk encryption
		- VPNs

		Hashing converts data into a fixed-length hash
		Password > Hash Function > Hash
		hello123 > SHA-256 > ef92b778
		Hashing is designed to be one-way
		Common hashing algorithms:
		- SHA-256
		- SHA-512
		- SHA-3
		for passwords, specialized paswword-hashing algorithms such as bcrypt,scrypt,Argon2 are commonly used.

<font color="#e36c09">Basic Memory Trick:</font>
		Encryption > Lock/Unlock
		Hashing > Fingerprint

## Symmetric vs Asymmetric Encryption

		Symmetric Encryption - where same key is used for encryption and decryption
		ex : AES , ChaCha20 > they are generally fast.

		Asymmetric Encryption - Uses two related key
		1. Public key 2. Private key
		Public key → can be shared & Private key → must be kept secret

## Firewall
	Controls network traffic according to security rules
	Internet > [Firewall] > Company Network 
	firewall can decide where allow or block the request
	Ex: Port 80 - allow ; Port 443 - allow ; port 23 - block
	firewall can exist as : Hardware,Software,Cloud/Network services

## Malware
		malware means malicious software intenionally designed to perform harmful or unauthorized actions.
		Major Types : 1. Virus 2. Worm 3. Trojan
		Virus > attaches itself to another file/program and typically requires execution to spread.
		Worm > can spread automatically across network or systems
		Trojan > Malicious software disguised as legitimate software

## Ransomware
		encrypts or otherwise locks access to data/systems and demands payment
		Files > Encrypted > 💰 Ransom demand

## Spyware
		secretly collects information about users or systems

## Rootkit
		Designed to maintain privilaged access while hiding its presence

## Phishing
		An attacker tries to trick you into giving sensitive information or performing an unsafe action.
		Ex: "Your bank account will be blocked. Click here immediately."

## Social Engineering