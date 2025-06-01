---
members:
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
  - Masumoto Kira
a_side: false
mv: false
type: 2nd Generation
tags:
  - song
  - start_over
released: 2023-06-28
order: "4"
name_eng: Industrial Complex
---
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

|   Row   |     Line-up      |
| :-----: | :--------------: |
| 2nd Row | 6 7 8 9 10 11 12 |
| 1st Row |    1 2 3 4 5     |

| Number |       Member        |   Number   |      Member       |
| :----: | :-----------------: | :--------: | :---------------: |
|   12   |  [[Takemoto Yui]]   |     6      |  [[Inoue Rina]]   |
|   11   |    [[Ozono Rei]]    |     5      | [[Matsuda Rina]]  |
|   10   | [[Fujiyoshi Karin]] |     4      | [[Yamasaki Ten]]  |
|   9    |   [[Tamura Hono]]   | 3 (center) | [[Masumoto Kira]] |
|   8    |   [[Moriya Rena]]   |     2      | [[Morita Hikaru]] |
|   7    | [[Kousaka Marino]]  |     1      |  [[Onuma Akiho]]  |


