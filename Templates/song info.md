## Info
```dataviewjs
if (typeof dv.current().name_eng != 'undefined') {
	let smth = "**English Title:** " + dv.current().name_eng
	dv.paragraph(smth);
}
if (typeof dv.current().choreographer != 'undefined') {
	let smth = "**Choreographer:** " + dv.current().choreographer
	dv.paragraph(smth);
}
if (typeof dv.current().director != 'undefined') {
	let smth = "**MV Director:** " + dv.current().director
	dv.paragraph(smth);
}
if (typeof dv.current().lyrics != 'undefined') {
	let smth = "**Lyrics:** " + dv.current().lyrics
	dv.paragraph(smth);
}
if (typeof dv.current().composer != 'undefined') {
	let smth = "**Composer:** " + dv.current().composer
	dv.paragraph(smth);
}
if (typeof dv.current().arranger != 'undefined') {
	let smth = "**Arranger:** " + dv.current().arranger
	dv.paragraph(smth);
}
```