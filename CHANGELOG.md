# v0.1.1

- Add new optional field "user_data" in schema, accepts arbitary string, your VM specific configuration can be stored here.
  Some 3rdparty tool expects certain content be set in this field.
  For example, [CiscoCloud/terraform.py](https://github.com/ccll/terraform.py) (a terraform-ansible bridging tool) interprete 'user_data' as a JSON string:
  ```
  {
    "role": "foobar",
    ...
  }
  ```
  It uses the 'role' field to group hosts.
