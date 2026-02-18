<div align="center" style="padding-bottom: 1rem">
  <img
    src="https://github.com/apisq.png"
    alt="apisq"
    height="200px"
    width="200px"
    style="
      width: 200px;
      height: 200px;
      object-fit: cover;
      border-radius: 16px;
      border: 2px solid #bdbdbd;
      box-shadow: 0 6px 16px rgba(0,0,0,0.15);
      display: block;
    "/>
</div>

# @apisq/bootstrap

Core resources for apisq applications & services.

**Not for direct deployment** - this stack should be deployed via `apisq/cli`.

## Resources

| Resource | Example | Description |
| ---- | ---- | ---- |
| `AssetsBucket` | `apisq-bootstrap-us-east-1-112233445566` | Bucket for code & other static resources to be stored & rendered from |
| `AssetsBucketKmsKey` | `<< KMS Key ID >>` | Customer-managed KMS key to encrypt the Assets bucket contents |
| `DeployRole` | `apisq-bootstrap-us-east-1-deploy-role` | Deployment role for Cloudformation to assume |
| `DeployPolicy1` | `apisq-bootstrap-us-east-1-deploy-policy-1` | Deployment policy for Cloudformation |
| `DeployPolicy2` | `apisq-bootstrap-us-east-1-deploy-policy-2` | Deployment policy for Cloudformation |
| `DeployPolicy3` | `apisq-bootstrap-us-east-1-deploy-policy-3` | Deployment policy for Cloudformation |
| `PermssionBoundaryPolicy` | `apisq-bootstrap-us-east-1-execution-permissions-boundary` | Execution permission boundary policy to limit what execution roles can do |
| `CustomDomain` | -- | Optionally, include a Custom Domain resource to attach API-Gateways to |

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
