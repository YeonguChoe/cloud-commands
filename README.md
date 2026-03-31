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

### Add Token

```bash
hcloud context create main
```

