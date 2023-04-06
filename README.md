TinyMCE multilanguage plugin
============================

[![Moodle Plugin CI](https://github.com/bfh/moodle-tiny_multilang2/workflows/Moodle%20Plugin%20CI/badge.svg?branch=master)](https://github.com/bfh/moodle-tiny_multilang2/actions?query=workflow%3A%22Moodle+Plugin+CI%22+branch%3Amaster)
![Release](https://img.shields.io/badge/release-v0.2.0-blue.svg)
![Supported](https://img.shields.io/badge/supported-4.1-green.svg)

This plugin will make the creation of multilingual contents on Moodle much easier with the TinyMCE editor.

The plugin is developed to work with [Iñaki Arenaza's multilang2 filter](https://github.com/iarenaza/moodle-filter_multilang2), and this plugin is the adaption 
on [his plugin for TinyMCE editor](https://github.com/iarenaza/moodle-tinymce_moodlelang2) and will work with TinyMCE 6
that is included in Moodle ≥ 4.1.

After the installation there is a new Button (with a globe icon) and a menu entry in the Format section where you can
select a language. Clicking on a language entry adds a language opening and closing tag to your text at the current
cursor position. If there is a selection then the language tags are places around the selection. In case you use the
highlighting option and see the yellow language tags, you may click one of these tags then select a new language
from the menu and that will change the language of the existing tag. You may also remove it by
hitting the backspace or delete key. This will remove the tag, and it's counterpart in case the formatting is correct.

## Current version

The latest release is v0.2.1 (build 2023040600) for Moodle 4.1 and newer.

## Requirements
The plugin [filter_multilang2](https://github.com/iarenaza/moodle-filter_multilang2) must be installed and enabled.

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
