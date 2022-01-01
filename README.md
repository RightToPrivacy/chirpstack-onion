    righttoprivacy[at]tutanota.com
    Blog: https://politictech.wordpress.com
    Mirror: https://www.buymeacoffee.com/politictech/posts

### WHY? 
 By default chirpstack web interface is http/cleartext. Running chirpstack-onion script
 creates an onion address for easy encryption management (Tor Browser).

 Other generic browser encryption certs may display confusing errors: .onion = security
 .onions are resistant to MITM attacks (Man in the Middle) using end to end between tor clients

 This script creates secure encryption keys + new .onion Tor Hidden Service Address
 
 Offering an end-to-end encryption option for secure Chirpstack LoRaWAN administration

### BENEFITS:
 * No MITM attacks on Chirpstack .onion
 * NAT punch: no need to change your firewall rules! 
 + no open ports - admin worldwide - securely

 Optional: block/reject outside localhost for .onion only access
 (hidden service only needs connection through localhost)

### REQUIREMENTS:

  Debian based operating system (ie: Armbian, Debian..) for the apt install tor line
 
### USAGE:
 
     sudo bash chirpstack-onion
     
     
 chirpstack-onion installs Tor + adds configuration for new onion connecting to port 8080 (Chirpstack),
 It then prints your new onion address to the screen after generating key + onion address.
 
 Open that .onion address in Tor Browser to login (or use standard local ip address).
 
 Block the local ip address (leave 127.0.0.1 open for Tor) for Tor Browser only Chirpstack.
