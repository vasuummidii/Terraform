provider "aws" {
    region = "ap-south-1"
    access_key = "AKIASPA75GGLWKPSALT5"
    secret_key = "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"
}

data "aws_ami" "app-ami" {
    most_recent = true
    owners = ["amazon"]
    filter {
        name = "name"
        values = ["amzn2-ami-hvm*"]
    }
}

resource "aws_instance" "myec2" {
    ami = data.aws_ami.app-ami.id
    instance_type = "t2.micro"
}
