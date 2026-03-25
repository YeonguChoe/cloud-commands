# Cloud commands



### SSH Key Generation

```bash
ssh-keygen -t rsa -b 2048 -f ./cloud-key
```

### Connecting to Cloud With SSH

```bash
ssh -i ./cloud-key username@hostname
```

### Change Linux User Password

```bash
passwd
```

### Download a File From Remote Server

```bash
scp -i ./cloud-key 
```
