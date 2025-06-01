Sakurazaka46's 3rd generation currently has  `$= dv.pages("#members/3").filter(x => x.status !== "Graduated").length` members:
```dataviewjs
let members = dv.pages('"Members/3ki"')
let active = members.filter(x => x.status === "Active");
let graduated = members.filter(x => x.status === "Graduated");
let hiatus = members = members.filter(x => x.status === "Hiatus");
let printing = ""

if (active.length != 0) {
	dv.paragraph("**Active (" + active.length + ")**")
}
for (i = 0; i < active.length; i++) {
	printing += active[i].file.link + ", "
}
dv.paragraph(printing.slice(0, -2))
printing = ""

if (hiatus.length != 0) {
	dv.paragraph("**On hiatus (" + hiatus.length + ")**")
}
for (i = 0; i < hiatus.length; i++) {
	printing += hiatus[i].file.link + ", "
}
dv.paragraph(printing.slice(0, -2))
printing = ""

if (graduated.length != 0) {
	dv.paragraph("**Graduated (" + graduated.length + ")**")
}
for (i = 0; i < graduated.length; i++) {
	printing += graduated[i].file.link + ", "
}
dv.paragraph(printing.slice(0, -2))
```
