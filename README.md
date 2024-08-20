#Introduction
This is predefined module which can be used to develop the Virtual Private Cloud in a very easy manner

##usage
```
module "vpc" {
    source = "./modules/VPC"

    vpc_config = {
      cidr_block = "10.0.0.0/16"
      name = "your-vpc"
    }
    subnet_config = {
      public_subnet={
        cidr_block="10.0.2.0/24"
        az="ap-south-1a"
        public=true
      }
      private_subnet={
        cidr_block="10.0.1.0/24"
        az="ap-south-1a"
      }
    }
  
}
```