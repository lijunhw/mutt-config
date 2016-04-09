# README

This folder hosts the templates for my mutt configurations. I place the whole folder as `$HOME/.mutts`. 

## Structure:

* `rc_templates`: muttrc file templates, consisting of one shared rc file (common) plus separate rc files for different mail accounts. These configuration templates have been tested against sending (saved to "Sent"), receiving, and drafting (IMAP sync'ed). 
* `signatures`: signature files
* `themes`: color themes making Mutt easier to read. 
* `rc`: instances based on `rc_templates`; not being git-tracked. 


## How to use it

```
git clone https://github.com/lijunhw/mutt_config.git
mv mutt_config ~/.mutts
cd ~/.mutts
mkdir rc
cp rc_templates rc/gmail_john  # make an instance of gmail config in rc_templates
vim rc/gmail_john  # do you editing here
mutt -F ~/.mutts/rc/gmail_john
```

