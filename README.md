# README

This folder hosts the templates for my mutt configurations. 

## Structure:

* `rc_templates`: muttrc file templates, consisting of one shared rc file (common) plus separate rc files for different mail accounts. These configuration templates have been tested against sending (saved to "Sent"), receiving, and drafting (IMAP sync'ed). 
* `themes`: color themes making Mutt easier to read. 
* `signatures`: signature files; not being git-tracked since they may contain personal information
* `rc`: instances based on `rc_templates`; not being git-tracked since they may contain personal credentials.


## How to use it

The default folder path is hard-coded to be `~/.mutts` so follow the procedure below:

```
git clone https://github.com/lijunhw/mutt_config.git
mv mutt_config ~/.mutts
cd ~/.mutts
mkdir rc signatures
cp rc_templates/gmail rc/gmail_john  # make an instance of gmail config in rc_templates
vim rc/gmail_john  # do you editing here
# optional 
# vim signatures/default.sig
mutt -F ~/.mutts/rc/gmail_john
```

I have also added [a post](http://ram.lijun.li/linux-mutt-another.html) on this setup. 
