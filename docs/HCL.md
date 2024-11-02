# HashiCorp Configuration Language (HCL)

HashiCorp Configuration Language (HCL) is a domain-specific language created by HashiCorp for defining infrastructure as code. HCL is designed to be both human-readable and machine-friendly, making it easier to understand and use for managing cloud resources.

## Key Features of HCL

1. **Human-Readable Syntax**: 
   - HCL is designed to be easily readable by humans, allowing users to quickly understand the configuration files. Its syntax resembles JSON but is more concise and expressive.

2. **Declarative Configuration**: 
   - HCL allows users to define the desired state of their infrastructure. You describe what you want, and HCL handles the necessary steps to achieve that state.

3. **Modularity**: 
   - HCL supports modules, enabling users to create reusable components. This promotes code reusability and better organization of configuration files.

4. **Variables and Outputs**: 
   - HCL supports variables, allowing users to parameterize configurations. Outputs can also be defined to extract information from resources, facilitating easier integration with other tools.

5. **Built-In Functions**: 
   - HCL includes a variety of built-in functions for manipulating data, performing calculations, and transforming input values, enhancing its flexibility and power.

## HCL Structure

HCL configurations consist of blocks, attributes, and arguments:

- **Blocks**: 
  - Represent a resource or a module. Each block begins with a block type (e.g., `resource`, `module`) followed by a label that identifies the specific instance.

- **Attributes**: 
  - Define properties of the block. Attributes are key-value pairs that specify configurations for resources.

- **Arguments**: 
  - Provide additional information or settings for blocks and attributes.

### Example of HCL Configuration

```hcl
provider "aws" {
  region = "us-west-2"
}

resource "aws_instance" "example" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t2.micro"

  tags = {
    Name = "ExampleInstance"
  }
}
