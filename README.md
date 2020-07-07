# hello-world
RSA keys are the most common ones and therefore the most compatible with
servers that may have an old OpenSSH version. Use them if the GitLab server
doesn't work with ED25519 keys.
The minimum key size is 1024 bits, defaulting to 2048. If you wish to generate a
stronger RSA key pair, specify the -b flag with a higher bit value than the
default.
The old, default password encoding for SSH private keys is
insecure;
it's only a single round of an MD5 hash. Since OpenSSH version 6.5, you should
use the -o option to ssh-keygen to encode your private key in a new, more
secure format.
If you already have an RSA SSH key pair to use with GitLab, consider upgrading it
to use the more secure password encryption format by using the following command
on the private key:


новая строчка с локалки