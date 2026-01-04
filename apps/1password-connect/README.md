# How to create OP_SESSION value

1. Download 1password-credentials.json from 1password 
2. Create secrets with the 1password-credentials.json file base64 encoded
```bash
echo "OP_SESSION=$(cat 1password-credentials.json| base64 -w0)" > secrets.1password.env
```
3. Encrypt secrets
```bash
sops encrypt secrets.1password.env > secrets.1password.enc.env
```
