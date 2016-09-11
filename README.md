# The Playbook
The playbook is a guide that gives current or potential clients and partners an overview of our operating and coding processes.

Please keep this information up-to-date as our processes evolve.

### Editing
To build the pdf you will need:
- pandoc (`brew install pandoc`)
- pdftk (https://www.pdflabs.com/tools/pdftk-server/)
- MacTex: (`brew cask install mactex`) note, this is kind of huge @ 2gb or so

To build the playbook:

```shell
rake build
```

To build and open the playbook:

```shell
rake preview
```

Thanks to thoughtbot for providing jumping off points for the latex template and rake tasks.

### Fonts
Install Roboto Slab from Google Fonts.

### Deploying
The built pdf and html directories should be uploaded to s3 and linked to on the main website. This should be automated, but it's not yet.
