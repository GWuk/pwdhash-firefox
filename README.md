# pwdhash-firefox
PwdHash extension for firefox

## description
Automatically generates per-site passwords if you prefix your password with @@ or press F2 beforehand.
Prevents JavaScript from reading your password as it is typed.
The same password will be generated at each subdomain: a.example.com matches b.example.com, a.example.co.uk
matches b.example.co.uk, but a.co.uk and b.co.uk are different.

Hashed passwords can also be generated at https://www.pwdhash.com/

## roadmap

* make it restartless (restructure code / migrate to jpm)
* create preferences dialog
* highlight password field if pwdhash is activated (optional)

## feature brainstorm

* activate for all password fields (press F2 to deactivate for current page, optional)

## changes in 2.0

* migration from XUL to WebExtension for e10s and support beyond Firefox 57
* added options page for PBKDF2-SHA512 support
* optionally use PBKDF2-SHA512 (based on https://www.cl.cam.ac.uk/~dl551/pwdhash/)
* mark active PwdHash with red border for PwdHash "legacy" mode and green border for PBKDF2-SHA512 mode
* Shift-F2 for "legacy" mode when PBKDF2-SHA512 enabled in options 
