---
members:
  - Morita Hikaru
  - Fujiyoshi Karin
  - Yamasaki Ten
  - Matono Mio
  - Taniguchi Airi
  - Moriya Rena
  - Tamura Hono
  - Yamashita Shizuki
  - Murayama Miu
  - Mukai Itoha
  - Ozono Rei
  - Matsuda Rina
  - Murai Yu
  - Ishimori Rika
center:
  - Morita Hikaru
mv: true
tags:
  - udagawa
  - song
type: Senbatsu
a_side: true
released: 2025-02-19
order: "1"
director: Ikeda Kazuma
Choreographer: TAKAHIRO
---
![](https://www.youtube.com/watch?v=qP52sh7PzYA)

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
----
## Formation

|   Row   |     Line-up      |
| :-----: | :--------------: |
| 3rd Row | 9 10 11 12 13 14 |
| 2nd Row |    4 5 6 7 8     |
| 1st Row |      1 2 3       |

| Number |      Member       | Number |        Member         |
| :----: | :---------------: | :----: | :-------------------: |
|   14   | [[Murayama Miu]]  |   7    |  [[Taniguchi Airi]]   |
|   13   |  [[Mukai Itoha]]  |   6    |    [[Moriya Rena]]    |
|   12   |   [[Ozono Rei]]   |   5    |    [[Tamura Hono]]    |
|   11   | [[Matsuda Rina]]  |   4    | [[Yamashita Shizuki]] |
|   10   |   [[Murai Yu]]    |   3    |  [[Fujiyoshi Karin]]  |
|   9    | [[Ishimori Rika]] |   2    |   [[Morita Hikaru]]   |
|   8    |  [[Matono Mio]]   |   1    |   [[Yamasaki Ten]]    |


----
## Performances
- https://www.youtube.com/watch?v=wRarTXZzDrs
