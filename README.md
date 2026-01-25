# @apisq/bootstrap

**Work in progress** - these stacks will be deployed via a CLI in the future. Until then, here's some lightweight docs.

```sh
$ aws cloudformation deploy \
  --region eu-west-2 \
  --stack-name apisq-assets \
  --template-file ./bootstrap.yml

$ aws cloudformation deploy \
  --region eu-west-2 \
  --stack-name apisq-deploy \
  --template-file ./iam-roles.yml \
  --capabilities CAPABILITY_NAMED_IAM
```
