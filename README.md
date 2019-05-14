# README

This folder hosts the templates for my mutt configurations. 

## Structure:

* `rc_templates`: muttrc file templates, consisting of one shared rc file (common) plus separate rc files for different mail accounts. These configuration templates have been tested against sending (saved to "Sent"), receiving, and drafting (IMAP sync'ed). 
* `themes`: color themes making Mutt easier to read. 
* `signatures`: signature files; not being git-tracked since they may contain personal information
* `rc`: instances based on `rc_templates`; not being git-tracked since they may contain personal credentials.


## Caveats

* Outlook.com configuration is not fully working (can get mails via IMAP but cannot sent via SMTP). 


## How to use it

The default folder path is hard-coded to be `~/.mutts` so follow the procedure below:

```
git clone https://github.com/lijuno/mutt_config.git
mv mutt_config ~/.mutts
cd ~/.mutts
mkdir rc signatures
cp rc_templates/gmail rc/gmail_john  # make an instance of gmail config in rc_templates
vim rc/gmail_john  # do you editing here
# vim signatures/default.sig   # add account-wide signature; optional
mutt -F ~/.mutts/rc/gmail_john
```

I also hadve [a post](http://d.lij.uno/linux-mutt-another.html) on this setup. 
