# Terraform Deployment
## Action: 
### Terraform Plan Output
[command]/home/runner/work/_temp/1e6c17a9-04b2-45fa-912b-be80b0363e45/terraform-bin plan -out=tfplan
[0m[1mmodule.vpc.aws_eip.nat_eip: Refreshing state... [id=eipalloc-0e49c387819f9953d][0m
[0m[1mmodule.vpc.aws_vpc.main: Refreshing state... [id=vpc-0e5ac2fb9b75cbfdf][0m
[0m[1maws_dynamodb_table.terraform_lock_table: Refreshing state... [id=terraform-lock-table][0m
[0m[1mmodule.vpc.aws_subnet.private_subnet_2: Refreshing state... [id=subnet-070395bb9cce7bca5][0m
[0m[1mmodule.vpc.aws_subnet.private_subnet_1: Refreshing state... [id=subnet-0afec064f734796d9][0m
[0m[1mmodule.vpc.aws_route_table.private_route_table: Refreshing state... [id=rtb-0c320e81f2a8b549b][0m
[0m[1mmodule.vpc.aws_internet_gateway.main: Refreshing state... [id=igw-03a2612ce9a4dd237][0m
[0m[1mmodule.vpc.aws_subnet.public_subnet_1: Refreshing state... [id=subnet-05761cfc269c22912][0m
[0m[1mmodule.vpc.aws_subnet.public_subnet_2: Refreshing state... [id=subnet-01177dcc419261fe9][0m
[0m[1mmodule.sg-group.aws_security_group.db_sg: Refreshing state... [id=sg-0cbefcd934e3df1be][0m
[0m[1mmodule.sg-group.aws_security_group.web_sg: Refreshing state... [id=sg-0c5c46bf08ae14365][0m
[0m[1mmodule.rds.aws_db_subnet_group.db_subnet_group: Refreshing state... [id=mysql-db-subnet-group][0m
[0m[1mmodule.vpc.aws_route_table.public_route_table: Refreshing state... [id=rtb-0de036d55c4989757][0m
[0m[1mmodule.vpc.aws_route_table_association.private_route_association_2: Refreshing state... [id=rtbassoc-098283604ce4e043f][0m
[0m[1mmodule.vpc.aws_route_table_association.private_route_association_1: Refreshing state... [id=rtbassoc-00dd642657fb840fa][0m
[0m[1mmodule.vpc.aws_nat_gateway.nat: Refreshing state... [id=nat-09a3dc91b79499c1c][0m
[0m[1mmodule.ec2.aws_instance.web_server_2: Refreshing state... [id=i-02115a23c3cee8a13][0m
[0m[1mmodule.ec2.aws_instance.web_server_1: Refreshing state... [id=i-0c5cc76f10d491907][0m
[0m[1mmodule.vpc.aws_route_table_association.public_route_association_2: Refreshing state... [id=rtbassoc-0123e0577d9c28a3f][0m
[0m[1mmodule.vpc.aws_route_table_association.public_route_association_1: Refreshing state... [id=rtbassoc-0204efbe2360fc81c][0m
[0m[1mmodule.vpc.aws_route.private_route_nat: Refreshing state... [id=r-rtb-0c320e81f2a8b549b1080289494][0m
[0m[1mmodule.rds.aws_db_instance.mysql_db: Refreshing state... [id=db-JOKXESLHTSYNAKGXOIGO2HZFEI][0m
[0m
[1m[36mNote:[0m[1m Objects have changed outside of Terraform[0m

[0mTerraform detected the following changes made outside of Terraform since the
last "terraform apply":

[1m  # module.sg-group.aws_security_group.db_sg[0m has been changed[0m[0m
[0m  [33m~[0m[0m resource "aws_security_group" "db_sg" {
        [1m[0mid[0m[0m                     = "sg-0cbefcd934e3df1be"
        [1m[0mname[0m[0m                   = "db-sg-20250417072235338600000003"
      [32m+[0m [0m[1m[0mtags[0m[0m                   = {}
        [90m# (9 unchanged attributes hidden)[0m[0m
    }
[1m  # module.sg-group.aws_security_group.web_sg[0m has been changed[0m[0m
[0m  [33m~[0m[0m resource "aws_security_group" "web_sg" {
        [1m[0mid[0m[0m                     = "sg-0c5c46bf08ae14365"
        [1m[0mname[0m[0m                   = "web-sg-20250417072235338100000002"
      [32m+[0m [0m[1m[0mtags[0m[0m                   = {}
        [90m# (9 unchanged attributes hidden)[0m[0m
    }
[1m  # module.vpc.aws_route_table.private_route_table[0m has been changed[0m[0m
[0m  [33m~[0m[0m resource "aws_route_table" "private_route_table" {
        [1m[0mid[0m[0m               = "rtb-0c320e81f2a8b549b"
      [33m~[0m [0m[1m[0mroute[0m[0m            = [
          [32m+[0m [0m{
              [32m+[0m [0mcarrier_gateway_id         = ""
              [32m+[0m [0mcidr_block                 = "0.0.0.0/0"
              [32m+[0m [0mcore_network_arn           = ""
              [32m+[0m [0mdestination_prefix_list_id = ""
              [32m+[0m [0megress_only_gateway_id     = ""
              [32m+[0m [0mgateway_id                 = ""
              [32m+[0m [0mipv6_cidr_block            = ""
              [32m+[0m [0mlocal_gateway_id           = ""
              [32m+[0m [0mnat_gateway_id             = "nat-09a3dc91b79499c1c"
              [32m+[0m [0mnetwork_interface_id       = ""
              [32m+[0m [0mtransit_gateway_id         = ""
              [32m+[0m [0mvpc_endpoint_id            = ""
              [32m+[0m [0mvpc_peering_connection_id  = ""
            },
        ]
      [32m+[0m [0m[1m[0mtags[0m[0m             = {}
        [90m# (5 unchanged attributes hidden)[0m[0m
    }
[1m  # module.vpc.aws_nat_gateway.nat[0m has been changed[0m[0m
[0m  [33m~[0m[0m resource "aws_nat_gateway" "nat" {
        [1m[0mid[0m[0m                                 = "nat-09a3dc91b79499c1c"
      [32m+[0m [0m[1m[0msecondary_allocation_ids[0m[0m           = []
        [1m[0mtags[0m[0m                               = {
            "Name" = "MyNATGateway"
        }
        [90m# (10 unchanged attributes hidden)[0m[0m
    }
[1m  # module.vpc.aws_eip.nat_eip[0m has been changed[0m[0m
[0m  [33m~[0m[0m resource "aws_eip" "nat_eip" {
      [32m+[0m [0m[1m[0massociation_id[0m[0m       = "eipassoc-09dba18532da858cb"
        [1m[0mid[0m[0m                   = "eipalloc-0e49c387819f9953d"
      [32m+[0m [0m[1m[0mnetwork_interface[0m[0m    = "eni-0112961e212800ff2"
      [32m+[0m [0m[1m[0mprivate_dns[0m[0m          = "ip-10-0-1-9.ec2.internal"
      [32m+[0m [0m[1m[0mprivate_ip[0m[0m           = "10.0.1.9"
      [32m+[0m [0m[1m[0mtags[0m[0m                 = {}
        [90m# (9 unchanged attributes hidden)[0m[0m
    }
[1m  # module.vpc.aws_route_table.public_route_table[0m has been changed[0m[0m
[0m  [33m~[0m[0m resource "aws_route_table" "public_route_table" {
        [1m[0mid[0m[0m               = "rtb-0de036d55c4989757"
      [32m+[0m [0m[1m[0mtags[0m[0m             = {}
        [90m# (6 unchanged attributes hidden)[0m[0m
    }
[1m  # module.rds.aws_db_instance.mysql_db[0m has been changed[0m[0m
[0m  [33m~[0m[0m resource "aws_db_instance" "mysql_db" {
      [32m+[0m [0m[1m[0mdomain_dns_ips[0m[0m                        = []
      [32m+[0m [0m[1m[0menabled_cloudwatch_logs_exports[0m[0m       = []
        [1m[0mid[0m[0m                                    = "db-JOKXESLHTSYNAKGXOIGO2HZFEI"
      [33m~[0m [0m[1m[0mlatest_restorable_time[0m[0m                = "2025-04-17T07:27:10Z" [33m->[0m [0m"2025-04-17T10:50:00Z"
        [1m[0mtags[0m[0m                                  = {
            "Name" = "MySQL RDS Instance"
        }
        [90m# (68 unchanged attributes hidden)[0m[0m
    }

Unless you have made equivalent changes to your configuration, or ignored the
relevant attributes using ignore_changes, the following plan may include
actions to undo or respond to these changes.
[90m
─────────────────────────────────────────────────────────────────────────────[0m

[0m[1m[32mNo changes.[0m[1m Your infrastructure matches the configuration.[0m

[0mYour configuration already matches the changes detected above. If you'd like
to update the Terraform state to match, create and apply a refresh-only plan:
  terraform apply -refresh-only
::debug::Terraform exited with code 0.
::debug::stdout: [0m[1mmodule.vpc.aws_eip.nat_eip: Refreshing state... [id=eipalloc-0e49c387819f9953d][0m%0A[0m[1mmodule.vpc.aws_vpc.main: Refreshing state... [id=vpc-0e5ac2fb9b75cbfdf][0m%0A[0m[1maws_dynamodb_table.terraform_lock_table: Refreshing state... [id=terraform-lock-table][0m%0A[0m[1mmodule.vpc.aws_subnet.private_subnet_2: Refreshing state... [id=subnet-070395bb9cce7bca5][0m%0A[0m[1mmodule.vpc.aws_subnet.private_subnet_1: Refreshing state... [id=subnet-0afec064f734796d9][0m%0A[0m[1mmodule.vpc.aws_route_table.private_route_table: Refreshing state... [id=rtb-0c320e81f2a8b549b][0m%0A[0m[1mmodule.vpc.aws_internet_gateway.main: Refreshing state... [id=igw-03a2612ce9a4dd237][0m%0A[0m[1mmodule.vpc.aws_subnet.public_subnet_1: Refreshing state... [id=subnet-05761cfc269c22912][0m%0A[0m[1mmodule.vpc.aws_subnet.public_subnet_2: Refreshing state... [id=subnet-01177dcc419261fe9][0m%0A[0m[1mmodule.sg-group.aws_security_group.db_sg: Refreshing state... [id=sg-0cbefcd934e3df1be][0m%0A[0m[1mmodule.sg-group.aws_security_group.web_sg: Refreshing state... [id=sg-0c5c46bf08ae14365][0m%0A[0m[1mmodule.rds.aws_db_subnet_group.db_subnet_group: Refreshing state... [id=mysql-db-subnet-group][0m%0A[0m[1mmodule.vpc.aws_route_table.public_route_table: Refreshing state... [id=rtb-0de036d55c4989757][0m%0A[0m[1mmodule.vpc.aws_route_table_association.private_route_association_2: Refreshing state... [id=rtbassoc-098283604ce4e043f][0m%0A[0m[1mmodule.vpc.aws_route_table_association.private_route_association_1: Refreshing state... [id=rtbassoc-00dd642657fb840fa][0m%0A[0m[1mmodule.vpc.aws_nat_gateway.nat: Refreshing state... [id=nat-09a3dc91b79499c1c][0m%0A[0m[1mmodule.ec2.aws_instance.web_server_2: Refreshing state... [id=i-02115a23c3cee8a13][0m%0A[0m[1mmodule.ec2.aws_instance.web_server_1: Refreshing state... [id=i-0c5cc76f10d491907][0m%0A[0m[1mmodule.vpc.aws_route_table_association.public_route_association_2: Refreshing state... [id=rtbassoc-0123e0577d9c28a3f][0m%0A[0m[1mmodule.vpc.aws_route_table_association.public_route_association_1: Refreshing state... [id=rtbassoc-0204efbe2360fc81c][0m%0A[0m[1mmodule.vpc.aws_route.private_route_nat: Refreshing state... [id=r-rtb-0c320e81f2a8b549b1080289494][0m%0A[0m[1mmodule.rds.aws_db_instance.mysql_db: Refreshing state... [id=db-JOKXESLHTSYNAKGXOIGO2HZFEI][0m%0A[0m%0A[1m[36mNote:[0m[1m Objects have changed outside of Terraform[0m%0A%0A[0mTerraform detected the following changes made outside of Terraform since the%0Alast "terraform apply":%0A%0A[1m  # module.sg-group.aws_security_group.db_sg[0m has been changed[0m[0m%0A[0m  [33m~[0m[0m resource "aws_security_group" "db_sg" {%0A        [1m[0mid[0m[0m                     = "sg-0cbefcd934e3df1be"%0A        [1m[0mname[0m[0m                   = "db-sg-20250417072235338600000003"%0A      [32m+[0m [0m[1m[0mtags[0m[0m                   = {}%0A        [90m# (9 unchanged attributes hidden)[0m[0m%0A    }%0A[1m  # module.sg-group.aws_security_group.web_sg[0m has been changed[0m[0m%0A[0m  [33m~[0m[0m resource "aws_security_group" "web_sg" {%0A        [1m[0mid[0m[0m                     = "sg-0c5c46bf08ae14365"%0A        [1m[0mname[0m[0m                   = "web-sg-20250417072235338100000002"%0A      [32m+[0m [0m[1m[0mtags[0m[0m                   = {}%0A        [90m# (9 unchanged attributes hidden)[0m[0m%0A    }%0A[1m  # module.vpc.aws_route_table.private_route_table[0m has been changed[0m[0m%0A[0m  [33m~[0m[0m resource "aws_route_table" "private_route_table" {%0A        [1m[0mid[0m[0m               = "rtb-0c320e81f2a8b549b"%0A      [33m~[0m [0m[1m[0mroute[0m[0m            = [%0A          [32m+[0m [0m{%0A              [32m+[0m [0mcarrier_gateway_id         = ""%0A              [32m+[0m [0mcidr_block                 = "0.0.0.0/0"%0A              [32m+[0m [0mcore_network_arn           = ""%0A              [32m+[0m [0mdestination_prefix_list_id = ""%0A              [32m+[0m [0megress_only_gateway_id     = ""%0A              [32m+[0m [0mgateway_id                 = ""%0A              [32m+[0m [0mipv6_cidr_block            = ""%0A              [32m+[0m [0mlocal_gateway_id           = ""%0A              [32m+[0m [0mnat_gateway_id             = "nat-09a3dc91b79499c1c"%0A              [32m+[0m [0mnetwork_interface_id       = ""%0A              [32m+[0m [0mtransit_gateway_id         = ""%0A              [32m+[0m [0mvpc_endpoint_id            = ""%0A              [32m+[0m [0mvpc_peering_connection_id  = ""%0A            },%0A        ]%0A      [32m+[0m [0m[1m[0mtags[0m[0m             = {}%0A        [90m# (5 unchanged attributes hidden)[0m[0m%0A    }%0A[1m  # module.vpc.aws_nat_gateway.nat[0m has been changed[0m[0m%0A[0m  [33m~[0m[0m resource "aws_nat_gateway" "nat" {%0A        [1m[0mid[0m[0m                                 = "nat-09a3dc91b79499c1c"%0A      [32m+[0m [0m[1m[0msecondary_allocation_ids[0m[0m           = []%0A        [1m[0mtags[0m[0m                               = {%0A            "Name" = "MyNATGateway"%0A        }%0A        [90m# (10 unchanged attributes hidden)[0m[0m%0A    }%0A[1m  # module.vpc.aws_eip.nat_eip[0m has been changed[0m[0m%0A[0m  [33m~[0m[0m resource "aws_eip" "nat_eip" {%0A      [32m+[0m [0m[1m[0massociation_id[0m[0m       = "eipassoc-09dba18532da858cb"%0A        [1m[0mid[0m[0m                   = "eipalloc-0e49c387819f9953d"%0A      [32m+[0m [0m[1m[0mnetwork_interface[0m[0m    = "eni-0112961e212800ff2"%0A      [32m+[0m [0m[1m[0mprivate_dns[0m[0m          = "ip-10-0-1-9.ec2.internal"%0A      [32m+[0m [0m[1m[0mprivate_ip[0m[0m           = "10.0.1.9"%0A      [32m+[0m [0m[1m[0mtags[0m[0m                 = {}%0A        [90m# (9 unchanged attributes hidden)[0m[0m%0A    }%0A[1m  # module.vpc.aws_route_table.public_route_table[0m has been changed[0m[0m%0A[0m  [33m~[0m[0m resource "aws_route_table" "public_route_table" {%0A        [1m[0mid[0m[0m               = "rtb-0de036d55c4989757"%0A      [32m+[0m [0m[1m[0mtags[0m[0m             = {}%0A        [90m# (6 unchanged attributes hidden)[0m[0m%0A    }%0A[1m  # module.rds.aws_db_instance.mysql_db[0m has been changed[0m[0m%0A[0m  [33m~[0m[0m resource "aws_db_instance" "mysql_db" {%0A      [32m+[0m [0m[1m[0mdomain_dns_ips[0m[0m                        = []%0A      [32m+[0m [0m[1m[0menabled_cloudwatch_logs_exports[0m[0m       = []%0A        [1m[0mid[0m[0m                                    = "db-JOKXESLHTSYNAKGXOIGO2HZFEI"%0A      [33m~[0m [0m[1m[0mlatest_restorable_time[0m[0m                = "2025-04-17T07:27:10Z" [33m->[0m [0m"2025-04-17T10:50:00Z"%0A        [1m[0mtags[0m[0m                                  = {%0A            "Name" = "MySQL RDS Instance"%0A        }%0A        [90m# (68 unchanged attributes hidden)[0m[0m%0A    }%0A%0AUnless you have made equivalent changes to your configuration, or ignored the%0Arelevant attributes using ignore_changes, the following plan may include%0Aactions to undo or respond to these changes.%0A[90m%0A─────────────────────────────────────────────────────────────────────────────[0m%0A%0A[0m[1m[32mNo changes.[0m[1m Your infrastructure matches the configuration.[0m%0A%0A[0mYour configuration already matches the changes detected above. If you'd like%0Ato update the Terraform state to match, create and apply a refresh-only plan:%0A  terraform apply -refresh-only%0A
::debug::stderr: 
::debug::exitcode: 0

::set-output name=stdout::[0m[1mmodule.vpc.aws_eip.nat_eip: Refreshing state... [id=eipalloc-0e49c387819f9953d][0m%0A[0m[1mmodule.vpc.aws_vpc.main: Refreshing state... [id=vpc-0e5ac2fb9b75cbfdf][0m%0A[0m[1maws_dynamodb_table.terraform_lock_table: Refreshing state... [id=terraform-lock-table][0m%0A[0m[1mmodule.vpc.aws_subnet.private_subnet_2: Refreshing state... [id=subnet-070395bb9cce7bca5][0m%0A[0m[1mmodule.vpc.aws_subnet.private_subnet_1: Refreshing state... [id=subnet-0afec064f734796d9][0m%0A[0m[1mmodule.vpc.aws_route_table.private_route_table: Refreshing state... [id=rtb-0c320e81f2a8b549b][0m%0A[0m[1mmodule.vpc.aws_internet_gateway.main: Refreshing state... [id=igw-03a2612ce9a4dd237][0m%0A[0m[1mmodule.vpc.aws_subnet.public_subnet_1: Refreshing state... [id=subnet-05761cfc269c22912][0m%0A[0m[1mmodule.vpc.aws_subnet.public_subnet_2: Refreshing state... [id=subnet-01177dcc419261fe9][0m%0A[0m[1mmodule.sg-group.aws_security_group.db_sg: Refreshing state... [id=sg-0cbefcd934e3df1be][0m%0A[0m[1mmodule.sg-group.aws_security_group.web_sg: Refreshing state... [id=sg-0c5c46bf08ae14365][0m%0A[0m[1mmodule.rds.aws_db_subnet_group.db_subnet_group: Refreshing state... [id=mysql-db-subnet-group][0m%0A[0m[1mmodule.vpc.aws_route_table.public_route_table: Refreshing state... [id=rtb-0de036d55c4989757][0m%0A[0m[1mmodule.vpc.aws_route_table_association.private_route_association_2: Refreshing state... [id=rtbassoc-098283604ce4e043f][0m%0A[0m[1mmodule.vpc.aws_route_table_association.private_route_association_1: Refreshing state... [id=rtbassoc-00dd642657fb840fa][0m%0A[0m[1mmodule.vpc.aws_nat_gateway.nat: Refreshing state... [id=nat-09a3dc91b79499c1c][0m%0A[0m[1mmodule.ec2.aws_instance.web_server_2: Refreshing state... [id=i-02115a23c3cee8a13][0m%0A[0m[1mmodule.ec2.aws_instance.web_server_1: Refreshing state... [id=i-0c5cc76f10d491907][0m%0A[0m[1mmodule.vpc.aws_route_table_association.public_route_association_2: Refreshing state... [id=rtbassoc-0123e0577d9c28a3f][0m%0A[0m[1mmodule.vpc.aws_route_table_association.public_route_association_1: Refreshing state... [id=rtbassoc-0204efbe2360fc81c][0m%0A[0m[1mmodule.vpc.aws_route.private_route_nat: Refreshing state... [id=r-rtb-0c320e81f2a8b549b1080289494][0m%0A[0m[1mmodule.rds.aws_db_instance.mysql_db: Refreshing state... [id=db-JOKXESLHTSYNAKGXOIGO2HZFEI][0m%0A[0m%0A[1m[36mNote:[0m[1m Objects have changed outside of Terraform[0m%0A%0A[0mTerraform detected the following changes made outside of Terraform since the%0Alast "terraform apply":%0A%0A[1m  # module.sg-group.aws_security_group.db_sg[0m has been changed[0m[0m%0A[0m  [33m~[0m[0m resource "aws_security_group" "db_sg" {%0A        [1m[0mid[0m[0m                     = "sg-0cbefcd934e3df1be"%0A        [1m[0mname[0m[0m                   = "db-sg-20250417072235338600000003"%0A      [32m+[0m [0m[1m[0mtags[0m[0m                   = {}%0A        [90m# (9 unchanged attributes hidden)[0m[0m%0A    }%0A[1m  # module.sg-group.aws_security_group.web_sg[0m has been changed[0m[0m%0A[0m  [33m~[0m[0m resource "aws_security_group" "web_sg" {%0A        [1m[0mid[0m[0m                     = "sg-0c5c46bf08ae14365"%0A        [1m[0mname[0m[0m                   = "web-sg-20250417072235338100000002"%0A      [32m+[0m [0m[1m[0mtags[0m[0m                   = {}%0A        [90m# (9 unchanged attributes hidden)[0m[0m%0A    }%0A[1m  # module.vpc.aws_route_table.private_route_table[0m has been changed[0m[0m%0A[0m  [33m~[0m[0m resource "aws_route_table" "private_route_table" {%0A        [1m[0mid[0m[0m               = "rtb-0c320e81f2a8b549b"%0A      [33m~[0m [0m[1m[0mroute[0m[0m            = [%0A          [32m+[0m [0m{%0A              [32m+[0m [0mcarrier_gateway_id         = ""%0A              [32m+[0m [0mcidr_block                 = "0.0.0.0/0"%0A              [32m+[0m [0mcore_network_arn           = ""%0A              [32m+[0m [0mdestination_prefix_list_id = ""%0A              [32m+[0m [0megress_only_gateway_id     = ""%0A              [32m+[0m [0mgateway_id                 = ""%0A              [32m+[0m [0mipv6_cidr_block            = ""%0A              [32m+[0m [0mlocal_gateway_id           = ""%0A              [32m+[0m [0mnat_gateway_id             = "nat-09a3dc91b79499c1c"%0A              [32m+[0m [0mnetwork_interface_id       = ""%0A              [32m+[0m [0mtransit_gateway_id         = ""%0A              [32m+[0m [0mvpc_endpoint_id            = ""%0A              [32m+[0m [0mvpc_peering_connection_id  = ""%0A            },%0A        ]%0A      [32m+[0m [0m[1m[0mtags[0m[0m             = {}%0A        [90m# (5 unchanged attributes hidden)[0m[0m%0A    }%0A[1m  # module.vpc.aws_nat_gateway.nat[0m has been changed[0m[0m%0A[0m  [33m~[0m[0m resource "aws_nat_gateway" "nat" {%0A        [1m[0mid[0m[0m                                 = "nat-09a3dc91b79499c1c"%0A      [32m+[0m [0m[1m[0msecondary_allocation_ids[0m[0m           = []%0A        [1m[0mtags[0m[0m                               = {%0A            "Name" = "MyNATGateway"%0A        }%0A        [90m# (10 unchanged attributes hidden)[0m[0m%0A    }%0A[1m  # module.vpc.aws_eip.nat_eip[0m has been changed[0m[0m%0A[0m  [33m~[0m[0m resource "aws_eip" "nat_eip" {%0A      [32m+[0m [0m[1m[0massociation_id[0m[0m       = "eipassoc-09dba18532da858cb"%0A        [1m[0mid[0m[0m                   = "eipalloc-0e49c387819f9953d"%0A      [32m+[0m [0m[1m[0mnetwork_interface[0m[0m    = "eni-0112961e212800ff2"%0A      [32m+[0m [0m[1m[0mprivate_dns[0m[0m          = "ip-10-0-1-9.ec2.internal"%0A      [32m+[0m [0m[1m[0mprivate_ip[0m[0m           = "10.0.1.9"%0A      [32m+[0m [0m[1m[0mtags[0m[0m                 = {}%0A        [90m# (9 unchanged attributes hidden)[0m[0m%0A    }%0A[1m  # module.vpc.aws_route_table.public_route_table[0m has been changed[0m[0m%0A[0m  [33m~[0m[0m resource "aws_route_table" "public_route_table" {%0A        [1m[0mid[0m[0m               = "rtb-0de036d55c4989757"%0A      [32m+[0m [0m[1m[0mtags[0m[0m             = {}%0A        [90m# (6 unchanged attributes hidden)[0m[0m%0A    }%0A[1m  # module.rds.aws_db_instance.mysql_db[0m has been changed[0m[0m%0A[0m  [33m~[0m[0m resource "aws_db_instance" "mysql_db" {%0A      [32m+[0m [0m[1m[0mdomain_dns_ips[0m[0m                        = []%0A      [32m+[0m [0m[1m[0menabled_cloudwatch_logs_exports[0m[0m       = []%0A        [1m[0mid[0m[0m                                    = "db-JOKXESLHTSYNAKGXOIGO2HZFEI"%0A      [33m~[0m [0m[1m[0mlatest_restorable_time[0m[0m                = "2025-04-17T07:27:10Z" [33m->[0m [0m"2025-04-17T10:50:00Z"%0A        [1m[0mtags[0m[0m                                  = {%0A            "Name" = "MySQL RDS Instance"%0A        }%0A        [90m# (68 unchanged attributes hidden)[0m[0m%0A    }%0A%0AUnless you have made equivalent changes to your configuration, or ignored the%0Arelevant attributes using ignore_changes, the following plan may include%0Aactions to undo or respond to these changes.%0A[90m%0A─────────────────────────────────────────────────────────────────────────────[0m%0A%0A[0m[1m[32mNo changes.[0m[1m Your infrastructure matches the configuration.[0m%0A%0A[0mYour configuration already matches the changes detected above. If you'd like%0Ato update the Terraform state to match, create and apply a refresh-only plan:%0A  terraform apply -refresh-only%0A

::set-output name=stderr::

::set-output name=exitcode::0
