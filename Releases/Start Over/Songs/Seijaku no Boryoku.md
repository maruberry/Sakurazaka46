---
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
center:
  - Yamashita Shizuki
a_side: false
mv: true
type: 3rd Generation
tags:
  - song
  - start_over
released: 2023-06-28
order: "2"
name_eng: Silnce is violence
---
![](https://youtu.be/uhbvX4GUrpE)


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

---
## Formation

|   Row   |  Line-up  |
| :-----: | :-------: |
| 3rd Row | 8 9 10 11 |
| 2nd Row |  4 5 6 7  |
| 1st Row |   1 2 3   |

| Number |        Member        |   Number   |        Member         |
| :----: | :------------------: | :--------: | :-------------------: |
|   11   |  [[Ishimori Rika]]   |     5      |  [[Taniguchi Airi]]   |
|   10   |  [[Odakura Reina]]   |     4      |   [[Murayama Miu]]    |
|   9    |   [[Mukai Itoha]]    |     3      |   [[Kojima Nagisa]]   |
|   8    |    [[Matono Mio]]    | 2 (center) | [[Yamashita Shizuki]] |
|   7    | [[Nakashima Yuzuki]] |     1      |     [[Murai Yu]]      |
|   6    |    [[Endo Riko]]     |            |                       |


