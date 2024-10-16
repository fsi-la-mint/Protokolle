<b>Sitzungsleitung: {{ page.leading }}</b>

<i>Protokoll: {{ page.protocol }}</i>

## Anwesenheit

<table>
<tr>
<th>Anwesend</th>
<th>Entschuldigt</th>
<th>Abwesend</th>
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
<td>
<ul>
{% for person in page.Abwesend %}
	<li> {{ person }} </li>
{% endfor %}
</ul>
</td>
</tr>
</table>

## Berichte aus der Universität
<table>
<tr>
<th>Gremium</th>
<th>Thema</th>
<th>Beschreibung</th>
</tr>

{% for theme in page.reports %}
<tr>
<td>{{ theme.committee }}</td>
<td>{{ theme.name }}</td>
<td>{{ theme.description | markdownify }}</td>
</tr>
{% endfor %}
</table>

## Offene Themen
<table>
<tr>
<th>Thema</th>
<th>Aktueller Stand</th>
<th>Besprechungsergebnis</th>
<th>Wer kümmert sich?</th>
</tr>

{% for theme in page.open_themes %}
<tr>
<td>{{ theme.name }}</td>
<td>{{ theme.current | markdownify }}</td>
<td>{{ theme.result | markdownify }}</td>
<td>{{ theme.responsible }}</td>
</tr>
{% endfor %}
</table>

## Neue Themen
<table>
<tr>
<th>Thema</th>
<th>Aktueller Stand</th>
<th>Besprechungsergebnis</th>
<th>Wer kümmert sich?</th>
</tr>

{% for theme in page.new_themes %}
<tr>
<td>{{ theme.name }}</td>
<td>{{ theme.description | markdownify }}</td>
<td>{{ theme.result | markdownify }}</td>
<td>{{ theme.responsible }}</td>
</tr>
{% endfor %}
</table>
