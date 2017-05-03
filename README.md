# electron-public
From smrt-systems/electron you can create new releases and with this repository you can promote them.

### Build and publish to staging
From smrt-systems/electron run

`npm run publish`

You need to have environment variable AWS_SECRET_ACCESS_KEY or ELECTRON_FORGE_S3_SECRET_ACCESS_KEY set.

### Promote new release
Edit the RELEASES file under the channel you want changed. Add new lines for each -delta and -full file up to the wanted version and keep it in order. Each line must contain

`{sha-1} {url} {file size}`

You can find all info here https://console.aws.amazon.com/s3/buckets/smrt-beta-electron/windows-update/

### Example promote qa to production
Copy RELEASES file from qa and paste in production folder.
