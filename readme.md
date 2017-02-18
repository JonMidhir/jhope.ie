# jhope.ie

My website, hosted on Amazon S3.

### Deploying

- Set Amazon S3 credentials into a passwd file in the local folder.

- Push changes to Github.

- Mount the bucket using `s3fs`:

```
    s3fs www.jhope.ie s3 -o passwd_file=./passwd
```

- Copy files to the bucket.
