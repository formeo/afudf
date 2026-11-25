# Install AFUDF

## Installation

* Windows: use the installer
* Linux: install the rpm or set manually
* For the database used to register functions execute SQL scripts registration

## Manual Installation

* Copy the files in the folder libraries {FireBird}\UDF
* Copy iconv.dll and afmmngr.dll  system folder windows\system32
* Linux: install [libiconv](http://www.gnu.org/software/libiconv/) from the repository
* Linux: ldconfig to configure afmmngr.so
* For the database used to register functions execute SQL scripts registration

## Firebird 4+ note

Starting with Firebird 4 UDF are deprecated and disabled by default
(`UdfAccess = None` in firebird.conf). Enable UDF access before registering
AFUDF functions:

```
UdfAccess = Restrict UDF
```

Restart the Firebird server after changing the configuration. The same is
required for Firebird 3.0 packages in modern Debian/Ubuntu (CVE-2025-65104
backport).
