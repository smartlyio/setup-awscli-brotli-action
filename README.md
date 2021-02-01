# setup-awscli-brotli-action

Inject brotli encoding file extension into Python's mimetypes db

## Usage


```
jobs:
  s3-upload:
    runs-on: ubuntu-latest
    steps:
      - name: Add brotli encoding to Python interpreter used by awscli
        uses: smartlyio/setup-awscli-brotli-action@master
      - name: Upload
        run: |
          # This will have the correct mimetype in the bucket, instead of binary/octet-stream
          aws s3 cp myfile.js.br s3://my-bucket/

```
