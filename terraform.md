# terraform script
```bash
provider "aws" {
  region = "ap-south-1"  
  access_key = "AKIA4T74ACGVL7RY4V56"
  secret_key = "rJmMPEAVmDStJXtNlyScDjGKrQFX/njCR1Z/e4zP"
}

resource "aws_instance" "example-1" {
  ami           = "ami-0187337106779cdf8"
  instance_type = "t2.micro"
  key_name = "mumbailinux"
  aws_security
  count = "1"
  tags = {
    Name = "ExampleInstance" 
  }
}
resource "aws_security_groups" "example-1" {
  tags = {
    Name = "ExampleInstance" 
  }
}
