resource "aws_instance" "master" {
  ami           = "ami-0fc5d935ebf8bc3bc"
  instance_type = var.instance_type
  key_name      = var.key_name
  subnet_id     = aws_subnet.k8s_subnet.id

  tags = {
    Name = "k8s-master"
  }
}

resource "aws_instance" "worker" {
  count         = 2
  ami           = "ami-0fc5d935ebf8bc3bc"
  instance_type = var.instance_type
  key_name      = var.key_name
  subnet_id     = aws_subnet.k8s_subnet.id

  tags = {
    Name = "k8s-worker-${count.index}"
  }
}
