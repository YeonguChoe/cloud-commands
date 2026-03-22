# Cloud commands



### SSH Key Generation

```bash
ssh-keygen -t rsa -b 2048 -f ./cloud-key
```

### Connecting to Cloud with ssh

```bash
ssh -i ./cloud-key username@hostname
```

### Change Linux User Password

```bash
passwd
```
