---
layout: docs-editor-guide
slug:
  - url: /docs/user-guide/editor
    label: editor
  - url: "/docs/user-guide/editor/workspace"
    label: "workspace"
  - "wires"
toc: toc-editor-guide.html
title: Wires
---

<div style="width: 435px" class="figure align-right">
  <img src="../images/editor-node-wire.png" alt="Node elements">
  <p class="caption">Wiring nodes</p>
</div>

Nodes are wired together by pressing the left-mouse button on a node's port, dragging
to the destination node and releasing the mouse button.

Alternatively, if the `Ctrl/Command` key is held down, the left-mouse
button can be clicked (and released) on a node's port and then clicked on the
destination. If the `Ctrl/Command` key remains held and the just-wired destination
node has an output port, a new wire is started from that port. This allows a
set of nodes to be quickly wired together.

This can also be combined with the Quick-Add dialog that is triggered
by a `Ctrl/Command-Click` on the workspace to quickly insert new nodes and have
them already wired to previous nodes in the flow.


#### Splitting wires

If a node with both an input and output port is dragged over the mid-point of a
wire, the wire is draw with a dash. If the node is then dropped, it is automatically
inserted into the flow at that point.

<div class="figure">
  <img src="../images/editor-wiring-splice.png" alt="">
  <p class="caption">Dropping a node on a wire to insert it mid-flow</p>
</div>

#### Moving wires

To disconnect a wire from a port, select the wire by clicking on it, then
press and hold the `Shift` key when the left-mouse button is pressed on the port.
When the mouse is then dragged, the wire disconnects from the port and can be
dropped on another port. If the mouse button is released over the workspace,
the wire is deleted.

If a port has multiple wires connected to it, if none of them is selected when
button is pressed with the `Shift` key held, all of the wires will move.

#### Selecting multiple wires

You can also select multiple wires by holding <kbd>ctrl</kbd> while clicking on them.

When you select multiple nodes, we also highlight any wires between them. This can make it easier to follow a flow once you have selected it.

<div class="figure">
  <img src="../images/select-multiple-wires.png" alt="">
  <p class="caption">Selecting multiple wires</p>
</div>


#### Deleting wires

1. Select one or more wires 
    1. To select a single wire, left click 1 wire.
    1. To select multiple wires, left click 1 wire then while holding <kbd>ctrl/⌘</kbd>, click on the other wires.
1. Press the <kbd>delete</kbd> key


#### Slicing wires
You can also remove wires by slicing through them. You do this by holding the ctrl (or cmd) key, then dragging the mouse with the right-hand button pressed:

<div class="figure">
  <img src="../images/slicing-wires.gif" alt="">
  <p class="caption">Slicing wires</p>
</div>


#### Detaching nodes

##### Delete Node, keep wires
You can delete a node from the middle of a flow and have the wiring automatically repair itself in the background:


<div class="row">
  <div class="figure column">
    <img src="../images/delete-node-keep-wires.gif" alt="">
    <p class="caption">Delete Node, keep wires</p>
  </div>
  <table class="action-ref double-column">
    <tr><th colspan="2">Reference</th></tr>
    <tr><td>Action</td><td><code>core:core:delete-selection-and-reconnect</code></td></tr>
    <tr><td>Key shortcut</td><td><kbd>Ctrl/⌘-delete</kbd></td></tr>
  </table>
</div>

##### Detach Node from wires
You can also detach a node from the flow without deleting it:

<div class="row">
  <div class="figure column">
    <img src="../images/detatch-node-from-wire.gif" alt="">
    <p class="caption">Detach Node from wires</p>
  </div>
  <table class="action-ref double-column">
    <tr><th colspan="2">Reference</th></tr>
    <tr><td>Action</td><td><code>core:detach-selected-nodes</code></td></tr>
    <tr><td>Key shortcut</td><td><code>*Not assigned</code></td></tr>
  </table>
</div>

<i>\* There is no default shortcut for **Detach Node from wires**, but you can assign one yourself in the Keyboard pane of the Settings dialog.</i> 