# WIS_ScriptDependencies

## Updates
1.2.0 (22 Nov 2024)

Finally, in the most recent versions of LiveCode, the browser widget is upgraded and can run Mermaid code! Hence the version number jump-up! :)
<ul>
<li>Enhancement: Flowcharts can now be displayed in the browser widget also on Windows, when using LC versions 9.6.13 (rc and stable), 10.0.0 (rc or stable) and all 10.0.1+ versions.</li>
<li>Enhancement: Added a settings pane for which handler types to include/exclude. The setting is global, not per project. Default is to include all handler types.</li>
<li>Enhancement: Implemented code formatting/colouring in the code display field</li>
<li>Fixed bug: Some flowchart nodes (handler names) were not correctly styled</li>
</ul>

1.1.7 (15 Jan 2024)
<ul>
<li>Fixed bug: In LC10, ”on” handlers did not get correct arrow colouring when highlighting the node</li>
<li>Enhancement/fix: Private functions now have the correct node colour, and a different node shape, to distinguish them from private commands</li>
</ul>

1.1.6 (12 Dec 2023)
<ul>
<li>Enhancement: If the Kroki service is down, so no png/svg can be produced, a dialog is presented giving the choice to render the flowchart as html instead</li>
<li>Enhancement: Improved design of the help section and the flowchart settings pane</li>
<li>Enhancement: Mermaid version can now be modified (affects html rendering only). This is not something you’d normally need to do, but it has turned out that the latest versions of Mermaid implement some kind of hard limit on the number of edges, preventing large flowcharts from rendering. So for now, Mermaid v10.5.1 is default (no edge limit), but can be changed to a later version by advanced users.</li>
<li>Fixed bug: Some actions in the mainstack triggered flowchart updates even if the flowchart substack was closed</li>
<li>Other minor fixes</li>
</ul>

1.1.5 (30 Nov 2023)
<ul>
<li>Enhancement: Flowcharts can now be produced and exported as PNG or SVG. On Windows and Linux the flowchart is now always displayed in-stack, as a PNG. On all platforms the flowchart can be exported as PNG, SVG and HTML.</li>
<li>Enhancement: Node text size can now be set</li>
<li>Adjustment: Handler type naming convention changed in LC10, making ”M” mean ”on” and ”C” mean ”command” (and changing ”PM” into ”PC” for ”private command”). This is now correctly handled when using WIS_ScriptDependencies in either LC9 or LC10.</li>
<li>Fixed bug: Arrow colouring failed for private commands/functions</li>
<li>Fixed bug: The (rarely used) constructions ”before *command name*" and  ”after *command name*” now get included in analysis and flowchart (displayed as ”command *command name*")</li>
<li>Other minor fixes</li>
</ul>

1.1.4 (12 Sep 2023)
<ul>
<li>Enhancement: Individual substacks can now be excluded from mapping/analysis by clicking the substack name in the stacks list. Excluded stacks/substacks are italic in the list.
(If a mainstack is excluded, its substacks are automatically excluded, like before.)</li>
</ul>

1.1.3 (27 Aug 2023)
<ul>
<li>Fixed bug: Saving user projects and settings didn’t trigger properly at closeStack. Now triggers at closeCard instead.</li>
<li>Enhancement: Handler analysis and comment stripping is now considerably faster to complete, especially in large projects</li>
<li>Enhancement: If a handler is selected in the Handler dependency stats field when creating a flowchart, all the arrows leading to and from that handler node will be coloured, to make them easier to follow. On MacOS, this will also happen when clicking a handler in the flowchart (in the browser widget).</li>
<li>Enhancement: Flowchart settings moved to its own settings pane, and node colours made modifiable</li>
</ul>

1.1.2 (22 Aug 2023)
<ul>
<li>Fixed bug: Commented-out handlers are now skipped when mapping relations</li>
<li>Fixed bug: Sometimes when upgrading from an earlier version, the user setting for char maximum of the flowchart syntax text could be empty, causing the flowchart to display only text</li>
<li>Enhancement: If a handler has more than one ”handler host”, i.e. resides in more than one script, the number of occurrences is shown in its flowchart node
<li>Other minor fixes</li>
</ul>

1.1.1 (20 Aug 2023)

<ul>
<li>Enhancement: Flowchart width limitation can now be turned off, to display the flowchart at actual size, instead of shrinking big charts to an unreadable size</li>
<li>Enhancement: Commands, functions and get/setProp nodes now have different colours to make them easier to distinguish between. Possibility for user selected colours will be implemented in a coming version.</li>
<li>Enhancement: In general settings it is now possible to increase the char maximum of the flowchart syntax text, to enable display of very large flowcharts. Only change this value if you get a "Maximum text size exceeded" error message in the flowchart.</li>
<li>Other minor fixes</li>
</ul>

1.1.0 (18 Aug 2023)

Enhancements:
<ul>
<li>A major overhaul of the stack selection feature. You can now save sets of stacks as ”projects” to easily switch between stack sets when running the analysis.</li>
<li>The flowchart settings have moved into the main UI, making flowchart customisation equally accessible on all platforms.</li>
<li>Project data and general settings are now saved to an lson file in the same folder when closing the stack. Any new version of the WIS_ScriptDependencies stack placed in the same folder will automatically restore your project data and general settings.</li>
</ul>
<ul>
<li>Fixed bug: No browser widgets will appear when using the stack on Linux, to prevent crashing</li>
<li>Other minor fixes</li>
</ul>

1.0.6 (13 Aug 2023)
<ul>
<li>Enhancement: Flowchart can now be exported to HTML file and launched in external browser. This is currently the only option for Windows users. Mac users get the in-stack interactive flowchart per default, but can choose to create an HTML file by pressing shift while clicking the Output flowchart button</li>
<li>Enhancement: Handlers that unambiguously reside in one single stack/card/control script can be grouped together in the flowchart view. This function can be toggled on/off</li>
<li>Enhancement: Possibility to filter out and filter in certain handlers. Filtering out some handlers , such as ”log” or mouse events can make some flowcharts less crowded</li>
<li>Enhancement: The stack now looks for newer versions of itself on startup</li>
<li>Other minor fixes</li>
</ul>

1.0.5 (11 Aug 2023)
<ul>
<li>Fixed bug: Stacks with . in their name didn’t trigger correctly from the Handler hierarchy list</li>
<li>Enhancement: Flowchart shapes for command, function, getProp/setProp improved</li>
<li>Enhancement: Presentation of the number of commands, functions, getProp/setProps</li>
<li>Enhancement: Better activity spinner</li>
<li>Other minor fixes</li>
</ul>

1.0.4 (10 August 2023) NB! The flowchart is currently not working on Windows! Investigation ongoing...
<ul>
<li>Enhancement: Possibility to output to flowchart. This adds a very cool new dimension to the tool, giving a visual representation of the script flows.</li>
</ul>

1.0.3 (10 May 2023)
<ul>
<li>Fixed bug: On Windows, only files with .livecodescript  or .rev would show up when selecting individual files for the list. Now .livecode files also appear.</li>
</ul>

1.0.2 (12 Apr 2023)

<ul>
<li>Fixed bug: runLookUp loop didn’t start over from the top node when searching, causing dependencies to be missed</li>
</ul>

1.0.1 (26 Mar 2023)

<ul>
<li>Fixed bug: Error occurred when selecting in tree view a stackname containing " of "</li>
<li>Fixed bug: Error when trying to filter certain empty lists</li>
<li>Enhancement: Better output report file naming</li>
</ul>
  
## Description
LiveCode tool for mapping and analysing script handler dependencies in your LiveCode projects

This is a developer tool for mapping and analysing LiveCode projects that may have many handlers and many stacks including library stacks etc.

The purpose is to see how the handlers interrelate and depend on each other, in order to find potential efficiency improvements or risk factors. As in, "How much will break if I mess up this handler?"

The handler dependency stats list is sorted in descending order of "popularity" - meaning that the handlers that most other handlers, or chains of handlers depend on, will be at the top. I’ve called that key value the ”dependency weight”. There might be better official terminology for such things, but anyway…

Note that there is no guarantee that the dependencies displayed are actually true. If you include two different unrelated stacks, which have similarly named handlers in them, dependencies will be claimed, but each stack is actually independent. 
So, to get a relevant analysis, include only stacks that belong to the same project, or are used by it.

The stack requires LiveCode v9.5+ to run. It only uses standard LiveCode controls and widgets.

This tool is free of charge, but if you like my work and want to suppport it you can buy me a coffee: https://www.buymeacoffee.com/riu9yazy7p
