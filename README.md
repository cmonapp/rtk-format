# rtk-format

Files with the .RTK extension are zip archives to be used by users of the RecetteTek application.

```
MyFile.rtk
├─ 827b9895-08cf-44e4-940b-728096968d4f.png //[uuid].png
├─ fc82033f-f5dd-4cfb-bb47-79e67d77aea9.png //[uuid].png
├─ recipes_0.json //max 400 recipes by file
├─ recipes_1.json //max 400 recipes by file
├─ recipes_2.json //max 400 recipes by file
├─ categories.json
├─ tags.json
├─ calendar.json
```

### Recipe file(s) : recipes_n.json

This file is a json array that contains max 400 recipes by file

You can use `\n` character to make a new line in alphanumeric fields

-   `title`  (required): recipe title
-   `description`: recipe description
-   `preparationTime` : recipe preparation time
-   `cookingTime`: recipe cooking time
-   `inactiveTime`: recipe inacative time
-   `totalTime`: recipe total time (Integer)
-   `ingredients`: recipe ingredients
-   `instructions`: recipe instructions
-   `pictures`: array contains zero or more pictures names
-   `url`: url of recipe
-   `video`: video of recipe (support automaticly youtube)
-   `notes`: recipe notes
-   `cookware`: recipe coookware
-   `nutrition`: recipe nutrition
-   `favorite`: is a favorite recipe (Boolean) 
-   `rating`: recipe rating (Float)
-   `categories`: array contains zero or more `Category`
-   `tags`: array contains zero or more `Tag`
-   `uuid`: unique identifier of recipe (Integer)
-   `lastModifiedDate`: recipe last modification date (YYYY-MM-DD HH:hh:ss)

Example :

```json
[
    {
       "title":"Title",
       "description":"Description",
       "preparationTime":"10",
       "cookingTime":"15",
       "inactiveTime":"12",
       "totalTime":"37",
       "quantity":"5",
       "ingredients":"ingredient1\ningredient2\ningredient3\n",
       "instructions":"instruction1\ninstruction2\ninstruction3\ninstruction4\n",
       "pictures":[
          "827b9895-08cf-44e4-940b-728096968d4f.png",
          "fc82033f-f5dd-4cfb-bb47-79e67d77aea9.png"
       ],
       "url":"https://en.m.wikibooks.org/wiki/Cookbook:Apple_Pie_I",
       "video":"https://youtu.be/NpEaa2P7qZI",
       "notes":"Comments",
       "cookware":"Cookware",
       "nutrition":"Nutrition",
       "favorite":true,
       "rating":3.0,
       "lastModifiedDate":"2020-09-10 08:39:09",
       "uuid":-1954851494,
       "categories":[
          {
             "title":"Categ1"
          },
          {
             "title":"Categ2"
          }
       ],
       "tags":[
          {
             "title":"tag1"
          },
          {
             "title":"tag2"
          }
       ]
    }
 ]
```

### Category file : categories.json
TODO

### Tag file : tags.json
TODO

### Calendar file : calendar.json
TODO

### Picture file(s) : [uuid].png
TODO
