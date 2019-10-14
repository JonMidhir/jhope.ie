# jhope.ie

My website, hosted on Amazon S3.

### Deploying

- Set Amazon S3 credentials into a passwd file in the local folder.

- Push changes to Github.

- Copy the files to S3 using the aws command line client:

```
  aws s3 sync . s3://www.jhope.ie
```
