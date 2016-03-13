# Syntax highlighting for Ansible

This package provides syntax highlighting for Sublime Text 2 and 3.

## Installation

To install this package, please do:


### Sublime Text 2

```
cd /tmp
wget -O sublime-ansible.tar.gz http://github.com/pchaigno/sublime-ansible/tarball/master
tar -xzvf sublime-ansible.tar.gz
mv pchaigno-sublime-ansible-*/*.tmLanguage ~/.config/sublime-text-2/Packages/User/
```


### Sublime Text 3 (Mac OS X)

```
cd /tmp
wget -O sublime-ansible.zip https://codeload.github.com/pchaigno/sublime-ansible/zip/master
unzip sublime-ansible.zip
zip -j Ansible.sublime-package sublime-ansible-master/*
mv Ansible.sublime-package ~/Library/Application\ Support/Sublime\ Text\ 3/Installed\ Packages/
```


### Install and configure ApplySyntax

ApplySyntax enables automatic recognition of Ansible files, based on their location.
Because Ansible files have a `.yml` extension, without ApplySyntax, they will be highlighted as YAML by default.

Installation:
```
Tools -> Command Palette... -> Package Control: Install Package
```

Path to Configuration:
```
Sublime Text -> Preferences -> Package Settings -> ApplySyntax -> Settings - User
```

And edit with syntax rules:
```
    "syntaxes": [
      {
        "name": "Ansible/Ansible",
        "rules": [
          {"file_name": ".*/tasks/.*.yml$"},
          {"file_name": ".*/handler/.*.yml$"},
          {"file_name": ".*/*_vars/.*.yml$"},
          {"file_name": ".*/roles/.*.yml$"},
          {"file_name": ".*/playbooks/.*.yml$"},
          {"file_name": ".*/.*ansible.*/.*.yml$"}
        ]
      },
```


## License

This package is under [MIT license](LICENSE).
