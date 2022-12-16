```
gpg --list-secret-keys --keyid-format=long
git config --get-regexp 'user\.*'
gpg --full-generate-key
gpg_id=$(gpg --list-secret-keys --keyid-format=long | sed -n '/^sec / s|.*/\([^ ]*\) .*|\1|p' | head)
gpg --armor --export ${gpg_id}
https://github.com/settings/gpg/new
```