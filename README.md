TinyMCE multilanguage plugin
============================

![Release](https://img.shields.io/badge/Release-0.3-blue.svg)
[![Moodle Plugin CI](https://github.com/bfh/moodle-tiny_multilang2/workflows/Moodle%20Plugin%20CI/badge.svg?branch=master)](https://github.com/bfh/moodle-tiny_multilang2/actions?query=workflow%3A%22Moodle+Plugin+CI%22+branch%3Amaster)
![Supported](https://img.shields.io/badge/Moodle-4.1+-orange.svg)
[![License GPL-3.0](https://img.shields.io/github/license/bfh/moodle-tiny_multilang2?color=lightgrey)](https://github.com/bfh/moodle-tiny_multilang2/blob/main/LICENSE)
[![GitHub contributors](https://img.shields.io/github/contributors/bfh/moodle-tiny_multilang2)](https://github.com/bfh/moodle-tiny_multilang2/graphs/contributors)

This plugin will make the creation of multilingual contents on Moodle much easier with the TinyMCE editor.

The plugin is developed to work with [Iñaki Arenaza's multilang2 filter](https://github.com/iarenaza/moodle-filter_multilang2), and this plugin is the adaption 
on [his plugin for TinyMCE editor](https://github.com/iarenaza/moodle-tinymce_moodlelang2) and will work with TinyMCE 6
that is included in Moodle ≥ 4.1.

After the installation of the plugin, the TinyMCE shows a new Button (with a globe icon) and a menu entry in the
"Format" section where you can select a language. Clicking on a language entry adds a language opening and closing
tag to your text at the current cursor position. If there is a selection then the language tags are places around
the selection. In case you use the highlighting option and see the yellow language tags, you may click one of these
tags then select a new language from the menu and that will change the
language of the existing tag. You may also remove it by  hitting the backspace
or delete key. This will remove the tag, and it's counterpart in case the
formatting is correct.

## Current version

The latest release is v0.3 (build 2023060600) for Moodle 4.1 and newer.

## Requirements

There are no additional requirements. To benefit from the plugin capabilities
the TinyMCE editor must be used in text area (either set as a user preference or
being the standard editor set by the Moodle site admin). Also, more than one
language must be active in your Moodle.
The plugin [filter_multilang2](https://github.com/iarenaza/moodle-filter_multilang2) is supported as well,
but it is not anymore a requirement to have it installed.

## Installation

 - Copy repository content in *moodleroot*/lib/editor/tiny/plugins. The following can be omitted:
   - tests/ (if you're not going to test it with Behat)
   - .gitmodules
   - build.xml
 - Install the plugin from Moodle. 

## Troubleshooting

If the language selection does not appear in the editor:
 - Check that the multilang2 filter is installed and enabled.
 - Check that your site has at least two languages installed.

## Version History

### 0.3

- Support for the standard language tags in Moodle without having to install the [filter_multilang2](https://github.com/iarenaza/moodle-filter_multilang2).
- Tooltip with possible languages is shown when a highlighted language tag is selected (only when `showalllanguages` is off, otherwise the tooltip list would be too long).
- Fix: when the text editor lost the focus the highlighting of the language tags disappeared.
- Fix: the iso code was not displayed in the language list in the menu when `showalllanguages` was enabled.
- Some internal refactoring because of the changes from above that made them necessary.
- Adjust behat tests to test both, standard annotation and multilang2 filter annotation.
- Change code maturity to RC.

### 0.2.3

- Fix links in README file and add license file.

### 0.2.2

- Lift software maturity level to STABLE.
- Adapt CI to test against Moodle 4.2.
- Fix issue [Probably, $string['helplinktext'] = 'Multi-Language Content (v2)'; is needed in the lang strings](https://github.com/bfh/moodle-tiny_multilang2/issues/1).
- Add version history to README file.

### 0.2.1

Initial release
