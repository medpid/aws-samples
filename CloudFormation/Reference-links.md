**Template Resource Type Reference**
* https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-template-resource-type-ref.html

**Diagram:** 
* https://lucid.app/lucidchart/f07d2df5-3d12-494f-b381-22d00fc59a9f/view?page=~OPYHuX1AnlW# 

**Template Snippets**
* https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/CHAP_TemplateQuickRef.html

**Ex: Full EC2 Instance**

https://raw.githubusercontent.com/natonic/CloudFormation-Deep-Dive/master/Labs/TemplateAnatomy/Template_Anatomy2.yaml


**VSCODE Setup for CloudFormation**

google-search - is to select and search plugin.

CloudFormation Linter - supports linting for CFN yaml.

YAML: https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml

Note: YAML needs a configuration to understand Intrinsic functions.

Add the below snippet to the settings.json

``` 
"yaml.customTags": [
        "!And",
        "!And sequence",
        "!If",
        "!If sequence",
        "!Not",
        "!Not sequence",
        "!Equals",
        "!Equals sequence",
        "!Or",
        "!Or sequence",
        "!FindInMap",
        "!FindInMap sequence",
        "!Base64",
        "!Join",
        "!Join sequence",
        "!Cidr",
        "!Ref",
        "!Sub",
        "!Sub sequence",
        "!GetAtt",
        "!GetAZs",
        "!ImportValue",
        "!ImportValue sequence",
        "!Select",
        "!Select sequence",
        "!Split",
        "!Split sequence",
        "!Condition",
        "!Transform sequence"
    ]
  ```

**CloudFormation Limits**

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cloudformation-limits.html



CloudFormation Main Elements:
        Metadata
        Parameters
        Mappings
        Conditions
        Transform
        Resources
        Ouputs

Topics
        Intrinsic functions
        Multiple Resources
        Pseudo Parameters
        Mappings
        Input Parameters
        Outputs

        Conditional Functions
        Change Sets

        Stack Sets


