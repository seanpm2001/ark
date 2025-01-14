# ark Cookbook CHANGELOG

This file is used to list changes made in each version of the ark cookbook.

## Unreleased

## 6.0.26 - *2023-10-03*

- Update README

## 6.0.25 - *2023-09-28*

## 6.0.24 - *2023-09-04*

## 6.0.23 - *2023-09-04*

## 6.0.22 - *2023-05-17*

## 6.0.21 - *2023-04-17*

## 6.0.20 - *2023-04-07*

Standardise files with files in sous-chefs/repo-management

## 6.0.19 - *2023-04-01*

## 6.0.18 - *2023-04-01*

## 6.0.17 - *2023-04-01*

Standardise files with files in sous-chefs/repo-management

## 6.0.16 - *2023-03-20*

Standardise files with files in sous-chefs/repo-management

## 6.0.15 - *2023-03-02*

- Remove private Chef boxes

## 6.0.14 - *2023-03-01*

- Update workflows to 2.0.1
- Remove mdl and replace with markdownlint-cli2

## 6.0.13 - *2023-02-23*

Standardise files with files in sous-chefs/repo-management

## 6.0.12 - *2023-02-16*

Standardise files with files in sous-chefs/repo-management

## 6.0.11 - *2023-02-15*

## 6.0.10 - *2023-02-15*

Standardise files with files in sous-chefs/repo-management

## 6.0.9 - *2023-02-14*

## 6.0.8 - *2023-02-14*

## 6.0.7 - *2023-02-13*

## 6.0.6 - *2023-02-13*

## 6.0.5 - *2022-12-15*

- Standardise files with files in sous-chefs/repo-management

## 6.0.4 - *2022-02-03*

- Update tested platforms
- Remove delivery and move to calling RSpec directly via a reusable workflow

## 6.0.3 - *2021-08-30*

- Standardise files with files in sous-chefs/repo-management

## 6.0.2 - *2021-06-18*

- Update location of test archive fixtures

## 6.0.1 - *2021-06-01*

- Standardise files with files in sous-chefs/repo-management

## 6.0.0 - *2021-05-22*

- Chef 17 updates: enable `unified_mode` on all resources
- Bump required Chef Infra Client to >= 15.3
- Migrate to using `seven_zip_tool` resource directly and require `seven_zip` >= 3.1
- Various ChefSpec fixes

## 5.1.1 - *2021-04-29*

- Added a version pin on seven_zip

## 5.1.0 - *2021-01-24*

- Sous Chefs Adoption
- Standardise files with files in sous-chefs/repo-management
- Cookstyle fixes
- Add integration testing for Windows and MacOS
- Remove testing for Amazon Linux 201x, CentOS 6 and Ubuntu 16.04
- Fix ChefSpec tests
- Fix issues with `--strip-components` with the `:cherry_pick` action on MacOS
- Ensure `/etc/profile.d` exists on MacOS if `append_env_path` is used

## 5.0.0 (2020-01-02)

- Require Chef Infra Client 14+ and remove the need for the build_essential dependency - [@tas50](https://github.com/tas50)
- Use Ruby classes in resource properties - [@tas50](https://github.com/tas50)
- Simplify the platform check logic - [@tas50](https://github.com/tas50)
- Remove the .foocritic file - [@tas50](https://github.com/tas50)
- Remove long_description and recipe metadata - [@tas50](https://github.com/tas50)
- Expand testing - [@tas50](https://github.com/tas50)
- Remove Ubuntu 14.04 testing - [@tas50](https://github.com/tas50)

## 4.0.0 (2018-07-25)

- Support append_env_path property on Windows, which increases the minimum required Chef release to Chef 13.4

## 3.1.1 (2018-07-24)

- Remove ChefSpec matchers since these are autogenerated now
- Update specs to the latest platform versions
- Remove template out of defaults directory
- Remove dependency on the Windows cookbook

## 3.1.0 (2017-05-06)

- Ensure the dependencies get installed on Chef 13 Amazon Linux systems
- Require Chef 12.7+ and remove action_class.class_eval usage

## 3.0.0 (2017-04-05)

- Rewrite of resource to custom resources.
- Remove EOL platforms from testing.
- Update zlib URL

## 2.2.1 (2016-12-16)

- Use Ohai root_group attribute to avoid trying to set the group to root on BSD/macOS.
- Add missing accessor for owner property

## 2.2.0 (2016-12-14)

- Add detection of .7z file extensions
- Fix 7zip extraction using strip_components >= 1 to properly extract to the path instead of the user's home_dir
- Always quote the path to the 7zip and xcopy binaries as they may have spaces
- Clarified in the readme that the install_with_make action includes the configure action
- Fix files with very long paths failing to extract on Windows
- Fix default owner of 'root' failing on Windows
- Fix 7-zip extraction with long paths when strip_components is >= 1
- Add the group attribute parameter to README
- Fix package installation failure on macOS systems
- Use x to extract with 7-zip, not e. Use e only for dump, which strips directories.

## 2.1.0 (2016-11-15)

- Move tar/7zip path logic out of attributes and into helpers to prevent failures when 7zip is not installed before the chef run starts
- Improve platform testing in Test Kitchen
- Recognize Windows as a supported platform in the readme
- Introduce a new attribute for overriding the 7-zip location: node['ark']['sevenzip_binary']

## 2.0.2 (2016-11-03)

- Fix suse support and centos < 6

## 2.1.0 (2016-11-01)

- Use multipackage installs to speed up installation
- Avoid installation package dependencies on Windows entirely
- Remove the testing bin stubs

## 2.0.0 (2016-09-15)

- Add CentOS 7.2, Fedora 23, and Suse specs
- Add centos 5, debian, and opensuse travis testing
- Add a contributing doc
- Fix cookstyle warnings
- Require Chef 12.1+

## [v1.2.0](https://github.com/chef-cookbooks/ark/tree/v1.2.0) (2016-07-03)

[Full Changelog](https://github.com/chef-cookbooks/ark/compare/v1.1.0...v1.2.0)

- Create seven_zip unpack command when strip_components is 0 [#155](https://github.com/chef-cookbooks/ark/pull/155) ([terkill](https://github.com/terkill))
- Get 7zip path from the windows registry. [#153](https://github.com/chef-cookbooks/ark/pull/153) ([buri17](https://github.com/buri17))
- Use fullpath for xcopy and icacls. [#152](https://github.com/chef-cookbooks/ark/pull/152) ([buri17](https://github.com/buri17))
- Define custom matcher helper for notification testing, fixes #139 [#144](https://github.com/chef-cookbooks/ark/pull/144) ([szymonpk](https://github.com/szymonpk))

## v1.1.0 (2016-05-19)

- Add support for RHEL 7
- Fixes to the readme to clarify actions / properties
- Expose the backup property in remote file to the ark resource
- Transfer the cookbook back to Chef
- Resolve all rubocop warnings
- Add maintainers files and Chef contributing docs
- Test on the latest platforms in .kitchen.yml and update Travis to use kitchen-dokken with additional platforms

## v1.0.1 (2016-02-16)

- Remove a large number of zero byte archives that snuck into the repository
- Remove a Chef 10 compatibility check in the custom resource

## v1.0.0 (2016-02-09)

- Added the pkg-config package to the debian platform family
- Added tar, xz-lzma-compat, and bzip2 packages to the RHEL and fedora platform families
- Updated FreeBSD to install gmake instead of make
- Added OS X, SmartOS, and FreeBSD to the tar path attributes to support those platforms
- Removed the has_binaries attribute from put action documentation in the readme file since this isn't supported there
- Moved the libraries module locations to no longer be under Opscode:: and broke out libraries into more logical units
- Fixed issues with spaces in Windows paths that could cause failures
- Fixed a bad attribute for the 7zip home on windows. Instead of using a node attribute use the value directly to avoid computed attribute overiding issues
- Switched from the 7-zip cookbook to seven_zip since the 7-zip cookbook is now deprecated
- Changed unzip commands to not use -u so that a newer archive can overwrite an existing directory
- Added support for actions py_setup, py_setup_install, py_setup_build
- Fixed setting home_dir attribute
- Added source_url and issues_url to the metadata.rb
- Expanded the supported platforms in metadata.rb
- Removed all references to Opscode
- Improved error logging when an unknown extension is encountered
- Added support for .tar files
- Improved overall testing:

   - Removed the kitchen.cloud.yml file and gem dependencies
   - Added integration testing in Travis with Kitchen-Docker and Travis tests now run using the nightly build of ChefDK
   - Expanded platforms tested in the .kitchen.yml file
   - Updated the Gemfile with the latest testing dependencies
   - Added full Chefspec coverage
   - Greatly expanded the ark_spec test cookbook
   - Removed the original minitests

- Added standard Chef .gitignore and chefignore files

- Resolved a large number of rubocop warnings

- Removed old Opscode contributing and testing docs

- Added a cookbook version badge to the readme

- Removed the Toftfile

## v0.9.0 (2014-06-06)

- [COOK-3642] Add Windows support

## v0.8.2 (2014-04-23)

- [COOK-4514] - Support for SLES with the Ark cookbook

## v0.8.0 (2014-04-10)

- [COOK-2771] - Add support for XZ compression

## v0.7.2 (2014-03-28)

- [COOK-4477] - Fix failing test suite
- [COOK-4484] - Replace strip_leading_dir attribute with more general strip_components

## v0.7.0 (2014-03-18)

- [COOK-4437] - configure and install_with_make should chown after unpack

## v0.6.0 (2014-02-27)

[COOK-3786] - Unable to install multiple versions of archive without duplication

## v0.5.0 (2014-02-21)

### Bug

- **[COOK-4288](https://tickets.opscode.com/browse/COOK-4288)** - Cleanup the Kitchen

### Improvement

- **[COOK-4264](https://tickets.opscode.com/browse/COOK-4264)** - Add node['ark']['package_dependencies'] to allow tuning packages.

## v0.4.2

### Improvement

- **[COOK-3854](https://tickets.opscode.com/browse/COOK-3854)** - Capability with mac_os_x: '/bin/chown' - No such file or directory
- Cleaning up some style for rubucop
- Updating test harness

## v0.4.0

### Improvement

- **[COOK-3539](https://tickets.opscode.com/browse/COOK-3539)** - Allow dumping of bz2 and gzip files

## v0.3.2

### Bug

- **[COOK-3191](https://tickets.opscode.com/browse/COOK-3191)** - Propogate unzip failures
- **[COOK-3118](https://tickets.opscode.com/browse/COOK-3118)** - Set cookbook attribute in provider
- **[COOK-3055](https://tickets.opscode.com/browse/COOK-3055)** - Use proper scope in helper module
- **[COOK-3054](https://tickets.opscode.com/browse/COOK-3054)** - Fix notification resource updating

### Improvement

- **[COOK-3179](https://tickets.opscode.com/browse/COOK-3179)** - README updates and refactor

## v0.3.0

### Improvement

- [COOK-3087]: Can't use ark with chef < 11

### Bug

- [COOK-3064]: `only_if` statements in ark's `install_with_make` and configure actions are not testing for file existence correctly.
- [COOK-3067]: ark kitchen test for `cherry_pick` is expecting the binary to be in the same parent folder as in the archive.

## v0.2.4

### Bug

- [COOK-3048]: Ark provider contains a `ruby_block` resource without a block attribute
- [COOK-3063]: Ark cookbook `cherry_pick` action's unzip command does not close if statement
- [COOK-3065]: Ark install action does not symlink binaries correctly

## v0.2.2

- Update the README to reflect the requirement for Chef 11 to use the ark resource (`use_inline_resources`).
- Making this a release so it will also appear on the community site page.

## v0.2.0

### Bug

- [COOK-2772]: Ark cookbook has foodcritic failures in provides/default.rb

### Improvement

- [COOK-2520]: Refactor ark providers to use the '`use_inline_resources`' LWRP DSL feature

## v0.1.0

- [COOK-2335] - ark resource broken on Chef 11

## v0.0.1

- [COOK-2026] - Allow `cherry_pick` action to be used for directories as well as files

## v0.0.1

- [COOK-1593] - README formatting updates for better display on Community Site

## v0.0.1

### Bug

- dangling "unless"

### Improvement

- add `setup_py_*` actions
- add vagrantfile
- add foodcritic test
- travis.ci support

## v0.0.10 (May 23, 2012

### Bug

- `strip_leading_dir` not working for zip files <https://github.com/bryanwb/chef-ark/issues/19>

### Improvement

- use autogen.sh to generate configure script for configure action <https://github.com/bryanwb/chef-ark/issues/16>
- support more file extensions <https://github.com/bryanwb/chef-ark/pull/18>
- add extension attribute which allows you to download files which do not have the file extension as part of the URL
