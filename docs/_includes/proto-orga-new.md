## TOP 0: Organisatorisches

<b>Sitzungsleitung: {{ page.leading }}</b>

<i>Protokoll: {{ page.protocol }}</i>

<table>
<tr>
<th>Anwesend</th>
<th>Entschuldigt</th>
</tr>
<tr>
<td>
<ul>
{% for person in page.Anwesend %}
	<li> {{ person }} </li>
{% endfor %}
</ul>
</td>
<td>
<ul>
{% for person in page.Entschuldigt %}
	<li> {{ person }} </li>
{% endfor %}
</ul>
</td>
</tr>
</table>
