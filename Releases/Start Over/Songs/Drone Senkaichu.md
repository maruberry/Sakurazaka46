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
  - Masumoto Kira
  - Matsuda Rina
  - Morita Hikaru
  - Moriya Rena
  - Yamasaki Ten
center:
  - Tamura Hono
a_side: false
mv: true
type: Senbatsu
tags:
  - song
released: 2023-06-28
order: "7"
director: Goto Shohei
Choreographer: TAKAHIRO
name_eng: Drone Circling
---
![](https://youtu.be/rNwzfyr07SM)

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

## Formation

|   Row   |       Line-up       |
| :-----: | :-----------------: |
| 3rd Row | 11 12 13 1415 16 17 |
| 2nd Row |     6 7 8 9 10      |
| 1st Row |      1 2 3 4 5      |

| Number |       Member       |   Number   |       Member        |
| :----: | :----------------: | :--------: | :-----------------: |
|   17   |  [[Saito Fuyuka]]  |     8      |   [[Habu Mizuho]]   |
|   16   | [[Kousaka Marino]] |     7      |  [[Kobayashi Yui]]  |
|   15   |   [[Ozono Rei]]    |     6      |  [[Matsuda Rina]]   |
|   14   |  [[Takemoto Yui]]  |     5      |  [[Yamasaki Ten]]   |
|   13   |   [[Inoue Rina]]   |     4      |   [[Moriya Rena]]   |
|   12   |  [[Uemura Rina]]   | 3 (center) |   [[Tamura Hono]]   |
|   11   |  [[Onuma Akiho]]   |     2      |  [[Morita Hikaru]]  |
|   10   | [[Masumoto Kira]]  |     1      | [[Fujiyoshi Karin]] |
|   9    |  [[Koike Minami]]  |            |                     |
