# `npm run deploy`

Deploys code in `/src` to `staging`. If `ARC_DEPLOY=production` is set, the code in `/src` will be deployed to `production`.

If the local `.arc` file has defined (and created) `@static` buckets, then the contents of `.static` are deployed to the appropriate S3 bucket. More about [working with static assets here](/guides/static-assets).

To use `npm run deploy`, add the following to your project's `package.json` scripts:

```json
{
  "scripts": {
    "deploy": "AWS_PROFILE={profile} AWS_REGION={region} arc-deploy",
  }
}
```

> Reminder: All `arc` npm run scripts require `AWS_PROFILE` and `AWS_REGION` environment variables set. Learn more in the [Prerequisites guide](/quickstart).