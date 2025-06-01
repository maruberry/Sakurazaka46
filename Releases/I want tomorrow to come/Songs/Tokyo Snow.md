---
members:
  - Ozono Rei
  - Takemoto Yui
  - Tamura Hono
  - Fujiyoshi Karin
  - Matsuda Rina
  - Morita Hikaru
  - Moriya Rena
  - Yamasaki Ten
  - Taniguchi Airi
  - Nakashima Yuzuki
  - Matono Mio
  - Mukai Itoha
  - Murayama Miu
  - Yamashita Shizuki
center:
  - Yamashita Shizuki
a_side: false
mv: false
type: Senbatsu
tags:
  - song
  - I_want_tomorrow
released: 2024-10-23
order: "7"
lyrics: Akimoto Yasushi
composer:
  - Tsuru Yuichiro
Arranger:
  - Tsuru Yuichiro
---
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
---- 
## Members Included
```dataviewjs
let members = dv.current().members
let info = dv.page("info")
members = members.map(x => dv.page(x))
let gens = []
for (let i = 1; i<=info.Generations; i++) {
	let smth = members.filter(x => x.generation == i)
	if (smth.length != 0) {
		gens.push(smth);
	}
}
for (let i = 0; i< gens.length; i++) {
	let text = ""
	if (gens[i][0].generation == 1) {
		text += "**" + gens[i][0].generation + "st Generation** ("
	}
	if (gens[i][0].generation == 2) {
		text += "**" + gens[i][0].generation + "nd Generation** ("
	}
	if (gens[i][0].generation == 3) {
		text += "**" + gens[i][0].generation + "rd Generation** ("
	}
	if (gens[i][0].generation == 4) {
		text += "**" + gens[i][0].generation + "th Generation** ("
	}
	text += gens[i].length + "): "
	for (let j = 0; j< gens[i].length; j++) {
		if (gens[i][j].name === dv.current().center) {
			text += gens[i][j].file.link + " (C), "
		}
		else {
			text += gens[i][j].file.link + ", "
		}
	}
	dv.paragraph(text.slice(0, -2))
}
```
