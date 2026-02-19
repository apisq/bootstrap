<div align="center">
  <img src="https://github.com/apisq.png" alt="apisq" height="100px" width="100px"/>
</div>

# @apisq/bootstrap

Core resources for apisq applications & services.

**Not for direct deployment** - this stack should be deployed via `apisq/cli`.

## Resources

| Resource | Example | Description |
| ---- | ---- | ---- |
| `AssetsBucket` | `apisq-bootstrap-us-east-1-112233445566` | Bucket for code & other static resources to be stored & rendered from |
| `DeployRole` | `apisq-bootstrap-us-east-1-deploy-role` | Deployment role for Cloudformation to assume |
| `DeployPolicy{N}` | `apisq-bootstrap-us-east-1-deploy-policy-{N}` | Deployment policies for Cloudformation |
| `PermssionBoundaryPolicy` | `apisq-bootstrap-us-east-1-execution-permissions-boundary` | Execution permission boundary policy to limit what execution roles can do |
| `CustomDomain` | — | Optionally, include a Custom Domain resource to attach API-Gateways to |

## Outputs

| Output | Name | Description |
| ---- | ---- | ---- |
| `Version` | `apisq-bootstrap-version` | Bootstrap version |
| `AssetsBucketName` | `apisq-bootstrap-assets-bucket` | Asset bucket name, for other stacks to deploy assets into |
| `AssetsBucketArn` | `apisq-bootstrap-assets-bucket-arn` | Asset bucket ARN, if required |
| `DeployRoleName` | `apisq-bootstrap-deploy-role` | Deploy role name, for other stacks to deploy resources with |
| `DeployRoleArn` | `apisq-bootstrap-deploy-role-arn` | Deploy role ARN, if required |
| `ExecutionPermissionsBoundary` | `apisq-bootstrap-permissions-policy` | Execution Permission Boundary name, for other stacks to include when creating new IAM roles |
| `CustomDomainName` | `apisq-bootstrap-custom-domain` | Custom Domain name |
| `CustomDomainArn` | `apisq-bootstrap-custom-domain-arn` | Custom Domain name ARN |

## Contributing

```sh
$ aws cloudformation deploy \
  --stack-name apisq-bootstrap \
  --template-file ./bootstrap.yml \
  --capabilities CAPABILITY_NAMED_IAM
```
