Self-Signed SSL Certificate
=========

The role that create a Self-Signed SSL certificate.

Master branch:
[![Build Status](https://travis-ci.org/timon2013/ansible_role_ssl_sign_cert.svg?branch=master)](https://travis-ci.org/timon2013/ansible_role_ssl_sign_cert)

Dev Branch:
[![Build Status](https://travis-ci.org/timon2013/ansible_role_ssl_sign_cert.svg?branch=dev)](https://travis-ci.org/timon2013/ansible_role_ssl_sign_cert)

Requirements
------------

```bash
meta/main.yml
```

Role Variables
--------------

String Bool
Default variables are in defaults directory.

| Name | Default               | Type          | Description                       |
| ---- | --------------------- | ------------- | ----------------------------------|
| `ssl_sign_cert_name` | defaults/main.yml     | String         | Certificate name         |
| `ssl_sign_cert_owner` | defaults/main.yml    | String         | Name of the user that should own the file/directory, as would be fed to chown. |
| `ssl_sign_cert_group` | defaults/main.yml    | String         | Name of the group that should own the file/directory, as would be fed to chown. |
| `ssl_sign_cert_csr_path` | defaults/main.yml    | String         | The name of the file into which the generated OpenSSL certificate signing request will be written.| `ssl_sign_cert_crt_path` | defaults/main.yml    | String         | Remote absolute path where the generated certificate file should be created or is already located. |
| `ssl_sign_cert_key_path` | defaults/main.yml    | String         | Name of the file in which the generated TLS/SSL private key will be written. It will have 0600 mode. |
| `packages_openssl` | defaults/main.yml    | Array | A package name or package specifier with version. |
| `ssl_sign_cert_key_type` | defaults/main.yml    | String | The algorithm used to generate the TLS/SSL private key. |
| `ssl_sign_cert_key_size` | defaults/main.yml    | String | Size (in bits) of the TLS/SSL key to generate. |
| `ssl_sign_cert_csr_digest` | defaults/main.yml    | String | The digest used when signing the certificate signing request with the private key.
| `ssl_sign_cert_email` | defaults/main.yml    | String | The emailAddress field of the certificate signing request subject. |
| `ssl_sign_cert_selfsigned_not_after` | defaults/main.yml    | String | The point in time at which the certificate stops being valid. |
| `ssl_sign_cert_get_to_local` | defaults/main.yml    | Bool | You can set "true" if you want download certificate and key to localhost. |
| `ssl_sign_cert_local_path_crt` | defaults/main.yml    | String | The local path where you want save certificate file. |
| `ssl_sign_cert_local_path_key` | defaults/main.yml    | String | The local path where you want save key file. |

Dependencies
------------

None

Example Playbook
----------------

```bash
molecule/default/playbook.yml
```

License
-------

MIT License

Author Information
------------------

timon2013
