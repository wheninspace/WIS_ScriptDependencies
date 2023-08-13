# WIS_ScriptDepedencies

## Updates
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
