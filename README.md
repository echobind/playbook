# The Playbook
The playbook is a guide that gives current or potential clients and partners an overview of our operating and coding processes.

Please keep this information up-to-date as our processes evolve.

### Editing
To build the pdf you will need:
- pandoc
- pdftk

To build the pdf:

```shell
rake build
```

To build and open the pdf:

```shell
rake preview
```

Thanks to thoughtbot for providing jumping off points for the latex template and rake tasks.

### Images
Currently, images need be uploaded to s3 as a pdf for inclusion in the project. This is because pandoc needs an absolute path or a url, and url’s will work across anyone’s setup.

### Deploying
The built pdf should be uploaded to s3 and linked to on the main website.
