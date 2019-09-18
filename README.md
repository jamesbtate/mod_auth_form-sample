# Apache httpd mod_auth_form sample
## Putting HTTPS and a pleasant login page backed by LDAP in front of a webapp that can't do network auth.

An example of how to use mod_auth_form with an LDAP backend, and proxying (most) requests to
another application. This example requires the user be a member of one of a few groups.
We are using HTTPS and the session cookie is encrypted. The logout URI of the proxied
application is intercepted and used to logout the user. The login page and stylesheet are
hosted in a fake path (`/httpd_auth/`) to make sure their names don't clash with the proxied
app.

