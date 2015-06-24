# Unfinished Docs

This is a table of symbols that have unfinished docs.  The goal is to have every column filled:

 <dl>

<dt>ref?</dt>
<dd>
if this is missing, there was no reference info auto-generated for the symbol. (the symbol must've come from an orphaned cljsdoc)
</dd>

<dt>cljsdoc?</dt>
<dd>
if this is missing, the symbol has no associated cljsdoc for adding a description, examples, and related symbols.
</dd>

<dt>examples?</dt>
<dd>
if this is missing, the symbol has no documented examples.
</dd>

<dt>related?</dt>
<dd>
if this is missing, the symbol has no "See Also" section (i.e. related symbols)
</dd>

</dl>

If a symbol has all aforementioned docs, then it is __removed__ from the table.

 <table>
<thead><tr>
<th>symbol</th>
<th>ref?</th>
<th>cljsdoc?</th>
<th>examples?</th>
<th>related?</th>
</tr></thead>

{{#symbols}}
<tr>
<td>{{&full-name}}</td>
<td>{{#ref}}[ref]({{&.}}){{/ref}}</td>
<td>{{#cljsdoc}}[cljsdoc]({{&.}}){{/cljsdoc}}</td>
<td>{{#examples}}:heavy_check_mark:{{/examples}}</td>
<td>{{#related}}:heavy_check_mark:{{/related}}</td>
</tr>
{{/symbols}}

</table>
