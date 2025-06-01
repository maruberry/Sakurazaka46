---
members:
  - Uemura Rina
  - Koike Minami
  - Kobayashi Yui
  - Saito Fuyuka
  - Habu Mizuho
center:
  - Koike Minami
a_side: false
mv: false
type: 1st Generation
tags:
  - song
  - start_over
released: 2023-06-28
order: "3"
name_eng: Sound of the Wind
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
## Formation

|   Row   |  Line-up  |
| :-----: | :-------: |
| 1st Row | 1 2 3 5 4 |

|   Number   |      Member      | Number |      Member       |
| :--------: | :--------------: | :----: | :---------------: |
|     5      | [[Saito Fuyuka]] |   2    | [[Kobayashi Yui]] |
|     4      | [[Habu Mizuho]]  |   1    |  [[Uemura Rina]]  |
| 3 (center) | [[Koike Minami]] |        |                   |

