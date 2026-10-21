# CloudFormation Validation Checklist

## Project
AWS VPC and EC2 Infrastructure

## Review checklist

- [ ] Confirm the YAML structure and CloudFormation resource types.
- [ ] Check that the VPC CIDR and subnet CIDR do not overlap incorrectly.
- [ ] Confirm that the subnet is associated with the intended route table.
- [ ] Verify that the Internet Gateway is attached to the VPC.
- [ ] Confirm that the EC2 instance references the intended subnet and security group.
- [ ] Review inbound and outbound security group rules.
- [ ] Confirm that the selected AMI is available in the target AWS Region.
- [ ] Review expected resource creation and possible costs before deployment.

## Security considerations

The template currently permits SSH from `0.0.0.0/0`. This is included for the educational exercise, but it is too permissive for normal production use. Restrict SSH access to an approved source range or use a suitable managed access method.

## Validation status

**Status:** Template saved to GitHub. Deployment and successful validation have not yet been confirmed.

No live AWS deployment should be assumed from the presence of this template in the repository.

## Next steps

1. Validate the template syntax.
2. Review security and networking configuration.
3. Deploy only in an authorized environment after checking permissions and costs.
4. Record actual results and add screenshots only after completing the corresponding checks.
