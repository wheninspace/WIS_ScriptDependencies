# WIS_ScriptDepedencies

## Updates

1.0.1 (26 Mar 2023)
Fixed bug: Error occurred when selecting in tree view a stackname containing " of "
Fixed bug: Error when trying to filter certain empty lists
Enhancement: Better output report file naming

## Description
LiveCode tool for mapping and analysing script handler dependencies in your LiveCode projects

This is a developer tool for mapping and analysing LiveCode projects that may have many handlers and many stacks including library stacks etc.

The purpose is to see how the handlers interrelate and depend on each other, in order to find potential efficiency improvements or risk factors. As in, "How much will break if I mess up this handler?"

The handler dependency stats list is sorted in descending order of "popularity" - meaning that the handlers that most other handlers, or chains of handlers depend on, will be at the top. I’ve called that key value the ”dependency weight”. There might be better official terminology for such things, but anyway…

Note that there is no guarantee that the dependencies displayed are actually true. If you include two different unrelated stacks, which have similarly named handlers in them, dependencies will be claimed, but each stack is actually independent. 
So, to get a relevant analysis, include only stacks that belong to the same project, or are used by it.

The stack requires LiveCode v9.5+ to run. It only uses standard LiveCode controls and widgets.
