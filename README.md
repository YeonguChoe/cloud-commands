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

## GCP
- Reference: https://docs.cloud.google.com/sdk/docs/cheatsheet

### Login related

- Login
```bash
gcloud auth login
```

- List logged-in accounts
```bash
gcloud auth list
```

- Logout
```bash
gcloud auth revoke <ACCOUNT>
```

### Project related

- List existing projects

```bash
gcloud projects list
```

- Check selected project

```bash
gcloud config get project
```

- Change selected project

```bash
gcloud config set project <PROJECT_ID>
```

### SSH connection

- Check existing instances

```bash
gcloud compute instances list
```

- Connect to instance

```bash
gcloud compute ssh <NAME>@<INSTANCE_NAME> --zone=<ZONE>
```

- Disconnect SSH connection

```bash
exit
```

- Add SSH login credential to `$HOME/.ssh/config`

```bash
gcloud compute config-ssh
```

## AWS

### Upload file from EC2 to S3

```bash
aws s3 cp <file> s3://<bucket>/<folder>/<file>
```

### Download file from S3 to EC2

```bash
aws s3 cp s3://<bucket>/<folder>/<file> .
```
