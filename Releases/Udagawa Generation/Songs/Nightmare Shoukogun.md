---
center:
  - Matono Mio
members:
  - Ishimori Rika
  - Endo Riko
  - Odakura Reina
  - Kojima Nagisa
  - Taniguchi Airi
  - Nakashima Yuzuki
  - Matono Mio
  - Mukai Itoha
  - Murai Yu
  - Murayama Miu
  - Yamashita Shizuki
mv: true
tags:
  - udagawa
  - song
type: 3rd Generation
a_side: 
released: 2025-02-19
order: "2"
director: Shun Murakami
Choreographer: TAKAHIRO
---
![](https://youtu.be/Grx5AhU14QU)

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
