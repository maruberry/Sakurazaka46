---
members:
  - Inoue Rina
  - Endo Hikari
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
center:
  - Fujiyoshi Karin
  - Yamasaki Ten
a_side: true
mv: true
type: Senbatsu
tags:
  - song
  - Addiction
released: 2025-04-30
order: "1"
director: Kato Hidejin
Choreographer: TAKAHIRO
---
![](https://youtu.be/ReuFa_D1Vok)

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

----
## Formation

|   Row   |          Line-up           |
| :-----: | :------------------------: |
| 3rd Row | 16 17 18 19 20 21 22 23 24 |
| 2nd Row |  7 8 9 10 11 12 13 14 15   |
| 1st Row |        1 2 3 4 5 6         |

| Number |       Member       |   Number   |        Member         |
| :----: | :----------------: | :--------: | :-------------------: |
|   24   | [[Odakura Reina]]  |     12     |  [[Taniguchi Airi]]   |
|   23   | [[Kousaka Marino]] |     11     |   [[Morita Hikaru]]   |
|   22   |  [[Onuma Akiho]]   |     10     |    [[Matono Mio]]     |
|   21   |   [[Endo Riko]]    |     9      |   [[Matsuda Rina]]    |
|   20   |   [[Inoue Rina]]   |     8      |   [[Ishimori Rika]]   |
|   19   |  [[Takemoto Yui]]  |     7      | [[Nakashima Yuzuki]]  |
|   18   | [[Masumoto Kira]]  |     6      | [[Yamashita Shizuki]] |
|   17   |  [[Endo Hikari]]   |     5      |     [[Murai Yu]]      |
|   16   | [[Kojima Nagisa]]  | 4 (center) |  [[Fujiyoshi Karin]]  |
|   15   |  [[Murayama Miu]]  | 3 (center) |   [[Yamasaki Ten]]    |
|   14   |  [[Mukai Itoha]]   |     2      |    [[Tamura Hono]]    |
|   13   |   [[Ozono Rei]]    |     1      |    [[Moriya Rena]]    |

