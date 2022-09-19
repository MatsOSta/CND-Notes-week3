# CND-Notes-week3

Application Hardening
Safest> disconnected
next best> flat files
dynamic content> danger

CIA no A

Common sense
restric what can run
restric who it can run as
restic what it can do
reach out of the network
read from the filesystem
write to a databe
load scripts or modules

WHY?
does your server have to "see" the net

APache webserver
is often at the edge of the network, commonly attacked

Guarding sensitive information
default config shows details about software version
OC hosting it
shows all errors, thus giving information to everyone.

Apache lists all the content of a directory unless there is an index file.
index.htm, index.html index.php
its enable to allow quick help

modules run by default and must be disabled and enabled.
isolate services if possible
what is apache running as
its own group and UID
shared role UID can rapidly become priviledges

apache needs it own non-priviledged account
config systems provision gid/uid and fs config
config server user http-web
group http-web

Restict access to directiores


HTTTP Security Headers
Headers are part of the http specification
defines the metadata of the message in both the http request and response
HTTP message body is often ment to be read by the user
Metadata is processed exclusivly by the web browser
since 1.0

Request data
languge of the request
cookies credentrial for the webiste
cache data

needed but dispized
X-XSS-Protection anit cross site scripting
X-Frame-Options clickjacking
X-content-type-options MIME
HTTP Strick Transport Security only SSH
Content Security Policy XSS clickjacking Code injection
X-permitted-cross-domain-policies 
Referred-Policy stops leaking url data
Feature-Policy can acces what features
HTTP public key pinning MITM
Expect-CT Fixes flaws in SSL/TLS

run the mysql security checks

