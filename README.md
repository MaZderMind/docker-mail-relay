Postfix Mail Relay
==================

Simple SMTP relay, based on [alterrebe/docker-mail-relay](https://github.com/alterrebe/docker-mail-relay)

Check out project above for usage instructions

Only minor changes have been made comparing to original project:

- smtpd TLS use is turned off (inside *postfix-main.cf* option *smtpd_use_tls=no*) to get rid of the problem with missing certificate.
  Everything else in *postfix-main.cf* was left untouched
  
- added truncation of newlines after filling *sasl_passwd* template with *j2*. It fixed some issues for me
