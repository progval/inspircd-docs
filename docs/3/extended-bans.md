---
title: v3 Extended Bans
---

## Extended Bans

Some [channel modes](/3/channel-modes/) (such as 'ban' or 'invite exception') accept nicknames or hostmasks as parameters. Using the extended ban parameters listed here lets you either match clients in more complex ways ('Matching' extbans) or changes the meaning of the mode ('Acting' extbans).

This lets you, for example, block CTCPs from matched users, match a specific user by their account name, and get more fine-grained control over how clients are moderated in a channel.

<table markdown="1">
<thead>
<tr>
<th>Character</th>
<th>Type</th>
<th>Ban Syntax</th>
<th>Module</th>
<th>Description</th>
</tr>
</thead>
<tbody markdown="1">
{% for extban in module_extbans|sort(attribute="char") %}
<tr markdown="1">
<td markdown="1">{{extban.char}}</td>
<td markdown="1">{{extban.type}}</td>
<td markdown="1">{% if extban.syntax == "None" %}<em>None</em>{% else %}{{extban.syntax}}{% endif %}</td>
<td markdown="1">[{{extban.module}}](/3/modules/{{extban.module}}/)</td>
<td markdown="1">{{extban.description}}</td>
</tr>
{% endfor %}
</tbody>
</table>
