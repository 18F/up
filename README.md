# Up
A simple script to encrypt and upload secrets to Amazon S3

*note*: This is still a work in progress. Don't use this to upload secret things yet

## Setup
Copy `up` to `/usr/local/bin/up`:

```bash
curl -o /usr/local/bin/up https://raw.githubusercontent.com/18F/up/master/up
```

Make `up` executable:

```bash
chmod +x /usr/local/bin/up
```

Set the requisite environmental variables:

```bash
export AWS_ACCESS_KEY=yourawsaccesskey
export AWS_SECRET_ACCESS_KEY=yoursecretaccesskey
export UP_BUCKET=targetbucketname
export UP_ENC_KEY=encryptionkeystring
```

## Usage

```bash
up filename
```

This will create `filename.enc` in the same directory and upload it to Amazon S3
