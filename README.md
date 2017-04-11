# Proyecto Final EDT | LDAP TLS SASL

## En que consisteix el proyecte ?

Partirem de la base que tothom te una base de [LDAP](https://es.wikipedia.org/wiki/OpenLDAP) , teorica o practica.
El que he fet ha sigut crear una infraestructura real amb _dockers_ del que podria ser una empresa o una escola.
Tota la comunicacio de dades sensibles entre els dockers es fa mitjançant TLS.

La meva idea es tenir tots els dockers monitoritçats amb un servidor Zabbix central instalat a un docker httpd i agents zabbix a cada docker. En especial en el docker del servidor _LDAP_ la meva intencio es fabricar uns scripts per redirigir dades de la _BBDD_
Monitor i aixi veure-ls a la interficie grafica.

### Tecnologies Emprades.

1. Openldap
  -- Amb Object Class:
    -- Per a Gestionar Users.
    -- Per a Gestionar Grups.
    -- Per a fer de DNS.
2. Docker
3. Cyrus-sasl(Per a la auth de GSSAPI)
  -- Implementades Autentificacions SASL GSSAPI(Ticket) y SASL External(Certificat).
4. Openssl
5. Supervisord
6. Nslcd
7. Kerberos
8. PAM
9. Zabbix Agentd y Zabbix Server

### Under Construction...

- [x] Zabbix Server Working in Ubuntu
- [ ] Put supervisord in all computers
- [ ] Put TLS on nslcd communication.
- [ ] Create a PAM for auth krb5 and/or unix ldap.
