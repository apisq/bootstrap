# @apisq/bootstrap

Core resources for apisq applications & services.

**Work in progress** - these stacks will be deployed via a CLI in the future. Until then, here's some lightweight docs.

```sh
$ aws cloudformation deploy \
  --stack-name apisq-bootstrap \
  --template-file ./bootstrap.yml \
  --capabilities CAPABILITY_NAMED_IAM
```
