[0.20+] Part Group & Filter
~~~~~~~~~~~~~~~~~~~~~~~~~~~

This is a little plugin for filtering editor parts. Filtering works via text
input and/or via user-defined categories and groups.

These are defined manually by user (using the provided editor). I originally
wanted to define the metrics on the fly, but I couldn’t find any reliable
way to make it work, so I opted for this approach instead. It takes some
time to properly prepare all the groups, but at least you have full control
over the filtering.

Installation:
~~~~~~~~~~~~~

Simply extract the archive into the GameData folder.

How to use:
~~~~~~~~~~~

Type text into the text box on the upper panel to filter parts by pattern
matching (name, manufacturer, description).

The "..." button toggles the group filtering window. This window shows part
groups sorted into categories (columns). User can select multiple groups
among multiple categories, the result filter is union/intersection of
selected groups, e.g. all stock parts AND (engines OR fuel tanks). Drag the
window title to move, drag the bottom right corner to resize.

Groups and categories can be modified using the provided editor, which can be
found at PartGroupsFilter\Tools\PartGroupsEditor.exe (requires .NET 4.0). You
can define/change existing categories by right clicking on the right panel
and add parts to them by dragging from the left panel. Don't forget to save.

To disable this feature, simply delete the PartGroupsFilter\Plugins\PluginData
folder. This also hides the "..." button, so you're effectively left with
just the text filter.

Positioning conflicts with other plugins can be resolved by editing the
PartGroupsFilter\Plugins\PluginData\config.xml file, look for filterTop,
filterLeft and filterWidth variables.

Changelog:
~~~~~~~~~~

v0.4 - fixed incompatibility with other addons

v0.3 - editor improvements:
     - fixed part loading issue: now loading all *.cfg files
     - columns can be toggled from the View menu
     - filtering using path
     - log can be copied using context menu

v0.2 - fixed issue with filter being removed when loading a rocket
     - positioning is now tweakable using the config.xml file

v0.1 - initial release
