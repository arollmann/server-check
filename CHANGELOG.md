# Changelog for Craft CMS Server Check

## 2.1.4 - 2022-04-16

### Added
- Added checks for relying on the default `@web` alias.

## 2.1.3 - 2022-02-15

### Added
- Added the BCMath extension as a requirement.

## 2.1.2 - 2022-02-14

### Changed
- Bumped the PHP requirement to 8.0.2+.

## 2.1.1 - 2022-02-10

### Fixed
- Fixed a bug where the MariaDB version wasn’t always being parsed correctly. ([craftcms/cms#10456](https://github.com/craftcms/cms/issues/10456))

## 2.1.0 - 2022-02-09

### Changed
- Bumped the PHP requirement to 8.0 for Craft 4.0.
- Bumped the PostgreSQL requirement to 10.0 for Craft 4.0.
- The `intl` extension is now required for Craft 4.0.

## 2.0.1 - 2021-12-07

### Added
- There is now an explicit check for MariaDB, and it requires version 10.2.7 or higher. 

## 1.2.1 - 2021-05-25

### Added
- Added a check for MySQL to see if the server has been configured with full timezone support.

## 1.2.0 2020-11-04

### Changed
- Bumped the PHP requirement to 7.2.5 for Craft 3.6.0.

## 1.1.9 - 2020-05-28

### Added
- Added `ignore_user_abort` as an optional method. 

## 1.1.8 - 2020-01-17

### Changed
- Changed the image extension check to make sure that if Imagick is installed, it can actually process images.

## 1.1.7 - 2019-01-31

### Added
- Added a new `max_execution_time` check.

### Changed
- External links now have `rel="noopener"`. ([#9](https://github.com/craftcms/server-check/pull/9))
- The `memory_limit` check now adds 1MB to the current value if not set to `-1`. ([#10](https://github.com/craftcms/server-check/pull/10))

## 1.1.6 - 2018-08-17

### Changed
- The `ctype` extension is now required because of Yii 2.x.

## 1.1.5 - 2018-08-14

### Changed
- The `iconv` extension is now required because of Twig 2.0.

## 1.1.4 - 2018-07-25

### Changed
- Added `proc_open`, `proc_close`, `proc_terminate`, and `proc_get_status` methods as optional.
- `allow_url_fopen` is now checked to see if it is enabled for Plugin Store and updating operations.

## 1.1.3 - 2018-07-18

### Changed
- The JSON extension is now required. ([#7](https://github.com/craftcms/server-check/issues/7))

## 1.1.2 - 2018-07-18

### Changed
- The Fileinfo extension is now required, not recommended. ([#6](https://github.com/craftcms/server-check/issues/6))
- Improved the wording of some requirement memos. ([#5](https://github.com/craftcms/server-check/issues/5))
- Removed the “Max Upload File Size” and “Max POST Size” requirement checks, as they weren’t actually checking anything.

## 1.1.1 - 2017-12-15

### Changed
- Links within requirement descriptions now open in a new window. ([craftcms/cms#2205](https://github.com/craftcms/cms/issues/2205))

## 1.1.0 - 2017-11-10

### Changed
- The requirements checker no longer attempts to parse a DB config file, and will only run DB requirement checks if a valid `dsn` is provided.
- Lots of refactoring

## 1.0.17 - 2017-06-29

### Changed
- `RequirementsChecker::checkWebRoot()` no longer checks if the `plugins/` folder is in the web root, as there is no `plugins/` folder. 

## 1.0.16 - 2017-06-19

### Changed
- `RequirementsChecker::checkWebRoot()` no longer checks if the `app/` folder is in the web root, as there is no `app/` folder.

## 1.0.15 - 2017-06-13

### Changed
- The DOM extension is now mandatory.

## 1.0.14 - 2017-05-07

### Fixed
- Fixed a bug where the script was considering a blank database password to be invalid. ([#4](https://github.com/craftcms/server-check/issues/4))

## 1.0.13 - 2017-05-01

### Changed
- Removed the PHP version requirement from `composer.json`.

## 1.0.12 - 2017-03-19

### Changed
- Craft 3 Beta 8 compatibility.

## 1.0.11 - 2017-03-07

### Fixed
- Fixed a bug where the PHP memory limit check would fail if `memory_limit` was set to `-1`, which means no limit. 

## 1.0.10 - 2017-02-21

### Fixed
- Fixed a bug where the requirements checker would error if the Craft project lived at the root of the file system.

## 1.0.9 - 2017-02-13

### Added
- Added the PHP `password_hash()` function as a mandatory requirement.
- Added the PHP Zip extension as a mandatory requirement.

## 1.0.8 - 2017-02-06

### Changed
- Tweaked keywords in composer.json 

### Fixed
- Fixed a bug where the default database port wasn’t being accounted for when connecting to the database.

## 1.0.7 - 2017-01-30

### Changed
- Updated the `support` properties in composer.json
- Craft 3 no longer requires `mcrypt`.

## 1.0.6 - 2017-01-17

### Added
- Added support for configuring the database port

## 1.0.5 - 2017-01-17

### Fixed
- Fixed a bug where `checkIniSet()` wasn’t undoing a change it made to PHP’s `memory_limit` setting.

## 1.0.4 - 2017-01-17

### Changed
- Craft 3 now requires PHP 7

## 1.0.3 - 2017-01-17

### Changed
- Updated code for latest Craft coding guidelines

### Removed
- Removed check for buggy `iconv` extension

## 1.0.2 - 2016-12-30

### Changed
- Autoloading support in composer.json

## 1.0.1 - 2016-12-30

### Changed
- No longer specifying a minimum stability in composer.json
- MIT license in composer.json

## 1.0.0 - 2016-12-30

Initial release.
