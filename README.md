[Categorization] of food by their common names.
> This is part of package [nvif1989].<br>
> Source: [Nutritive Value of Indian Foods 1989].

```javascript
const groups = require('@nvif1989/groups');
// groups.corpus: Map {code => {code, group, entries, tags}}
// groups.load(): true (corpus loaded)
// groups.sql([table], [options]): sql commands
// groups.csv(): path to csv file
// groups(<query>)
// -> [{code, group, entries, tags}] for matched groups


groups.load();
/* load corpus first */

groups('cereals');
groups('Grains');
groups('505a');
// [
//   {
//     code: 'A',
//     group: 'Cereal grains and products',
//     entries: '1-27;452-465;505a',
//     tags: 'vegetarian eggetarian fishetarian veg'
//   }
// ]

groups('what is vegetable?');
groups('vegetable group code?');
// [
//   {
//     code: 'C',
//     group: 'Leafy vegetables',
//     entries: '47-114;469-507',
//     tags: 'vegetarian eggetarian fishetarian veg'
//   },
//   {
//     code: 'D',
//     group: 'Other vegetables',
//     entries: '137-188;525-543',
//     tags: 'vegetarian eggetarian fishetarian veg'
//   }
// ]

groups('47');
// [
//   {
//     code: 'C',
//     group: 'Leafy vegetables',
//     entries: '47-114;469-507',
//     tags: 'vegetarian eggetarian fishetarian veg'
//   }
// ]

groups('543');
// [
//   {
//     code: 'D',
//     group: 'Other vegetables',
//     entries: '137-188;525-543',
//     tags: 'vegetarian eggetarian fishetarian veg'
//   }
// ]
```


[![nvif1989](https://i.imgur.com/mGVou5c.png)](https://www.npmjs.com/package/nvif1989)
> You can ask about composition of 592 key foods in India here: [nvif1989.github.io].<br>
> Food composition values were measured by [National Institute of Nutrition, Hyderabad].<br>
> Take a peek at the raw data here: [Document], [Webpage].

[nvif1989]: https://www.npmjs.com/package/nvif1989
[Nutritive Value of Indian Foods 1989]: https://www.icmr.nic.in/content/nutritive-value-indian-foods-nvif-c-gopalan-b-v-rama-sastri-sc-balasubramanian-revised
[Categorization]: https://github.com/nvif1989/groups/blob/master/index.csv
[nvif1989.github.io]: https://nvif1989.github.io
[National Institute of Nutrition, Hyderabad]: https://www.nin.res.in/
[Document]: https://docs.google.com/spreadsheets/d/1a1uTkfoyaQeGpSB_20NtIiKibABYOF7w0EErscrgibw/edit?usp=sharing
[Webpage]: https://docs.google.com/spreadsheets/d/e/2PACX-1vTff_Ezvu3vMtB3vwSuyq2Y6Yop8-lhx3_XpJTsawKe-rcXC6KbfwSSeykM59Nbu7s3r2AYaRIHxH8J/pubhtml
