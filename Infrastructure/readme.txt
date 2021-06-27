### Finding Ubuntu Images with the AWS SSM Parameter Store ###

    *** Get the latest AMI id of the specific AMI
        aws ssm get-parameters --names \
                /aws/service/canonical/ubuntu/PRODUCT/RELEASE/stable/current/ARCH/VIRT_TYPE/VOL_TYPE/ami-id \
            --query 'Parameters[0].[Value]' --output text

        Where the fields are as follows:

            - PRODUCT: server or server-minimal
            - RELEASE: focal, 20.04, bionic, 18.04, xenial, or 16.04
            - ARCH: amd64 or arm64
            - VIRT_TYPE: pv or hvm
            - VOL_TYPE: ebs-gp2, ebs-io1, ebs-standard, or instance-store 

        Examples: 
            aws ssm get-parameters --names \
                    /aws/service/canonical/ubuntu/server/18.04/stable/current/amd64/hvm/ebs-gp2/ami-id \
                --query 'Parameters[0].[Value]' --output text

### Finding Windows Images with the AWS SSM Parameter Store ###

    *** Get the public SSM Parameter AWS Windows AMIs
        aws ssm get-parameters-by-path --path "/aws/service/ami-windows-latest" --region us-east-1

    *** Get the latest AMI id of the specific AMI
        aws ssm get-parameters --names /aws/service/ami-windows-latest/Windows_Server-2019-English-Full-Base --region ap-southeast-2 \
            --query 'Parameters[0].[Value]' --output text

### Finding Amazon Linux Images with the AWS SSM Parameter Store ###   

    *** Get the list of all Linux AMI in the current AWS region:
        aws ssm get-parameters-by-path --path /aws/service/ami-amazon-linux-latest --query "Parameters[].Name"

    *** Get the latest AMI id of the specific AMI:
        aws ssm get-parameters --names /aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2 --region ap-southeast-2 \
            --query 'Parameters[0].[Value]' --output text    

