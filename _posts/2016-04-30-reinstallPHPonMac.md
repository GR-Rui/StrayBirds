---
layout: post
title: Mac下重新编译安装PHP问题
category: PHP
comments: true
---

### configure: error: Cannot find libz

```

RaytekiMacBook-Pro:~ ray$ sudo brew install php55 --with-gmp --with-imap --with-tidy --with-debug --with-mysql=/usr/local/mysql --without-snmp
Password:
==> Installing php55 from josegonzalez/php
==> Downloading https://php.net/get/php-5.5.34.tar.bz2/from/this/mirror
Already downloaded: /Library/Caches/Homebrew/php55-5.5.34
==> ./configure --prefix=/usr/local/Cellar/php55/5.5.34 --localstatedir=/usr/loc
Last 15 lines from /Users/ray/Library/Logs/Homebrew/php55/01.configure:
checking for Kerberos support... /usr
checking for krb5-config... /usr/bin/krb5-config
checking for DSA_get_default_method in -lssl... no
checking for X509_free in -lcrypto... yes
checking for RAND_egd... no
checking for pkg-config... no
checking for OpenSSL version... >= 0.9.6
checking for CRYPTO_free in -lcrypto... yes
checking for SSL_CTX_set_ssl_version in -lssl... yes
checking for PCRE library to use... bundled
checking whether to enable the SQLite3 extension... yes
checking bundled sqlite3 library... yes
checking for ZLIB support... yes
checking if the location of ZLIB install directory is defined... no
configure: error: Cannot find libz

READ THIS: https://git.io/brew-troubleshooting
If reporting this issue please do so at (not Homebrew/brew):
  https://github.com/josegonzalez/homebrew-php/issues

Error: Your OS X keychain GitHub credentials do not have sufficient scope!
Scopes they have: []
Create a personal access token: https://github.com/settings/tokens
and then set HOMEBREW_GITHUB_API_TOKEN as the authentication method instead.
/System/Library/Frameworks/Ruby.framework/Versions/2.0/usr/lib/ruby/2.0.0/open-uri.rb:353:in `open_http': 422 Unprocessable Entity (GitHub::Error)
Validation Failed
```

you can try: ```xcode-select --install``` that seems to fix this issue for everyone that has had it so far. even if you have installed Xcode a different way
