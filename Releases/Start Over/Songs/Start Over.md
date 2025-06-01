---
members:
  - Uemura Rina
  - Koike Minami
  - Kobayashi Yui
  - Saito Fuyuka
  - Habu Mizuho
  - Inoue Rina
  - Ozono Rei
  - Onuma Akiho
  - Kousaka Marino
  - Takemoto Yui
  - Tamura Hono
  - Fujiyoshi Karin
  - Morita Hikaru
  - Moriya Rena
  - Yamasaki Ten
  - Masumoto Kira
  - Matsuda Rina
center:
  - Fujiyoshi Karin
a_side: true
mv: true
type: Senbatsu
tags:
  - song
  - start_over
released: 2023-06-28
order: "1"
name_eng: Start Over
lyrics: Akimoto Yasushi
director: Kato Hidejin
---
![](https://www.youtube.com/watch?v=YJRFD1AdaUE)

Start over senbatsu features all of the active at the time 1st and 2nd generation members (Except [[Endo Hikari]] Who was on hiatus). This is also the last single without any 3rd generation members in the senbatsu. 

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

## Included members
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
----
## Formation

|   Row   |       Line-up       |
| :-----: | :-----------------: |
| 3rd Row | 11 12 13 1415 16 17 |
| 2nd Row |     6 7 8 9 10      |
| 1st Row |      1 2 3 4 5      |

| Number |       Member       |   Number   |       Member        |
| :----: | :----------------: | :--------: | :-----------------: |
|   17   |   [[Inoue Rina]]   |     8      |  [[Kobayashi Yui]]  |
|   16   |  [[Onuma Akiho]]   |     7      |  [[Koike Minami]]   |
|   15   |  [[Uemura Rina]]   |     6      |  [[Masumoto Kira]]  |
|   14   |   [[Ozono Rei]]    |     5      |  [[Morita Hikaru]]  |
|   13   | [[Kousaka Marino]] |     4      |  [[Yamasaki Ten]]   |
|   12   |  [[Saito Fuyuka]]  | 3 (center) | [[Fujiyoshi Karin]] |
|   11   |  [[Takemoto Yui]]  |     2      |   [[Tamura Hono]]   |
|   10   |  [[Matsuda Rina]]  |     1      |   [[Moriya Rena]]   |
|   9    |  [[Habu Mizuho]]   |            |                     |

----
## Performances

- https://youtu.be/qSeSDsuhpSE
