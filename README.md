srr_motd Cookbook
===================
Sets the message of the day on Linux servers.


Requirements
------------
Linux OS


Attributes
----------
default['srr_motd']['motd'] = "This system is managed by Chef. Manual modifications may be overwritten."
#### srr_motd::default
<table>
  <tr>
    <th>Key</th>
    <th>Type</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td><tt>['srr_motd']['motd']</tt></td>
    <td>String</td>
    <td>The message to display when logging in to a Linux system</td>
    <td><tt>"This system is managed by Chef. Manual modifications may be overwritten."</tt></td>
  </tr>
</table>

Usage
-----
#### srr_motd::default

## Use a wrapper cookbook ##
In your metadata.rb: add the line 'depends srr_motd'
In your recipes/default.rb: add the line 'include_recipe srr_motd'
In your attributes/default.rb: Override any attributes you like.

Or, just include `srr_motd` in your node's `run_list`:

```json
{
  "name":"my_node",
  "run_list": [
    "recipe[srr_motd]"
  ]
}
```


License and Authors
-------------------
Authors: Steven Riggs
