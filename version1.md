interface versions {
    name: string,
    date: Date,
    Bugs: string[] | string,
    features: string[] | string,
    Author: string,
    Type: string[] | string
}
//enum for type of the versions
enum IversionsType { Patch, Major, Enhancement }
//interface for Bugs
interface IBugId {
    bugId: string,
    bug: string[]
}
//versions Data
const Data: versions[] = [{
    name: "samsung.F11",
    date: new Date('02-07-2020'),
    Type: "major",
    features: ["search"],
    Author: "william",
    Bugs: ['ABC21', "video"]
},{
    name: "apple-version1",
    date: new Date('06-07-2019'),
    Type: "major",
    features: ["device stability improvements", "search"],
    Bugs: ['ABC84', "Audio"],
    Author: "Steve_jobs"
},

{
    name: "Kiwi-version3",
    date: new Date('06-07-2019'),
    Type: "patch",
    features: ["new enhanced features"],
    Bugs: ['ABC85', "Video"],
    Author: "Brian Acton"
},

{
    name: "Grapes-version5.F",
    date: new Date('06-07-2019'),
    Type: "enhancement",
    features: ["Security-By-Design Approach"],
    Bugs: ['ABC86', "crash button after tap"],
    Author: "Bran Acton"
},

{
    name: "orange-version2.0",
    date: new Date('06-07-2019'),
    Type: "patch",
    features: ["Auto Rotation Animation"],
    Bugs: ['ABC87', "Poor UX Writing practices"],
    Author: "Sergey Brin"
},

{
    name: "kitkat-version7.A",
    date: new Date('06-07-2019'),
    Type: "enhancement",
    features: ["new enhanced features"],
    Bugs: ['ABC88', "Visualization problems"],
    Author: "Sergey Brin"
}]
// console.table(Data)
//Identifing Type in versions:-
let Patch = (Data.filter(n => n.Type.includes("patch")))
let Major = (Data.filter(n => n.Type.includes("major")))
let Enhancement = (Data.filter(n => n.Type.includes("enhancement")))
console.log("Type of patch in versions",  ["Patch"])
console.log("Type of major in versions", ["major"])
console.log("Type of enhancement in versions", Enhancement)
//Identifying date in versions:-
var year = Data.filter(a => a.date.toString().includes("1999"))
console.log("particular year in versions", year)
//Identifying author in versions:-
var arr1: string[] = []
Data.forEach(version => {
    arr1.push(version.Author)
})
arr = []
var arr = [...new Set(arr1)]
let releaseArr = []
for (let index of arr1) {
    let release = 0
    for (let index1 of arr1) {
        if (index === index1) {
            release++
        }
    }
    releaseArr.push(release)
}
let max = Math.max(...releaseArr)
for (let key in releaseArr) {
    if (max === releaseArr[key]) {
        console.log("Maximum Number of Author in Versions:-",arr[key]);
    }

}
// Identifying Bugs :-
let giveId:string= "ABC88"
for (let index in Data) {
    if (giveId === Data[index].Bugs[0]) {
       var id:any= (Data[index])
    }
}
console.log([id], "bugid")

# version
