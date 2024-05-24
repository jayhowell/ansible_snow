Service Now Ansible Change Request.
=========

This Ansible task which normally gets used in the Advanced Cluster Manager Ansible demo is used with the book import application located at https://github.com/levenhagen/book-import/blob/prehook/book-import/prehook/snow-create-change-record.yaml

If you fork the repository above, make sure you fork the prehook branch.  That's where the magic happens. 

Caviats
-------
Becuase I've use variables in the task file main.yml, you must use the following json when testing the template or it will fail.  These variables will normally be fed in from the prehook call to ansible in the above snow-create-change-record.yaml

```json
{
  "app_name": "myapp",
  "change_request": {
    "description": "The following resources have been updated: [...]",
    "justification": "We need to update this app"
  }
}
