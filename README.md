# Cloud commands

### SSH Key Generation

```bash
ssh-keygen -b 2048 -f <key>.pem -m PEM -t rsa
```

### Change Permission of SSH Key File

```bash
chmod 600 <key>.pem
```

### Connecting to Cloud With SSH

```bash
ssh -i ./cloud-key -o PubKeyAcceptedAlgorithms=+ssh-rsa username@hostname
```

- If server does not allow ssh-rsa, add `-o PubKeyAcceptedAlgorithms=+ssh-rsa`

```bash
ssh -i ./cloud-key -o PubKeyAcceptedAlgorithms=+ssh-rsa username@hostname
```

### Change Linux User Password

```bash
passwd
```

### Upload file to Remote Server

```bash
scp -i <ssh-key> <file-to-upload> <username>@<host>:<path>
```

### Compress folder with LZ4

```bash
tar --use-compress-program=lz4 -cf <file-name>.tar.lz4 <folder-name>/
```

### Decompress folder with LZ4

```bash
tar --use-compress-program=lz4 -xf <file-name>.tar.lz4
```
