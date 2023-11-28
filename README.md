This page is made to explain the exchange formats used by My Recipe Box - RecetteTek

# RTK format (.rtk)

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
# Sync folder

When you use synchronisation in app, the pictures and a recettetek.data file are present in your sync folder.
recettetek.data is also a zip archive.
The sync folder is use only for sync process, it is not meant to be changed by users

```
├─ 827b9895-08cf-44e4-940b-728096968d4f.png //[uuid].png
├─ fc82033f-f5dd-4cfb-bb47-79e67d77aea9.png //[uuid].png
recettetek.data
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

| Attribute Name       | Description                            | Type      | Required |
|----------------------|----------------------------------------|-----------|----------|
| `uuid`               | Unique identifier of the recipe (dce2a77a-ff62-4a8c-a087-05d9300c6665) | String    | Yes      |
| `title`              | Recipe title                           | String    | Yes      |
| `description`        | Recipe description                     | String    | No       |
| `preparationTime`    | Recipe preparation time                | String    | No       |
| `cookingTime`        | Recipe cooking time                    | String    | No       |
| `inactiveTime`       | Recipe inactive time                   | String    | No       |
| `totalTime`          | Total recipe time (in minutes)         | Integer   | No       |
| `ingredients`        | Recipe ingredients                     | String    | No       |
| `instructions`       | Recipe instructions                    | String    | No       |
| `pictures`           | Names of pictures                      | [String]  | No       |
| `url`                | URL of the recipe                      | String    | No       |
| `video`              | Recipe video                           | String    | No       |
| `notes`              | Notes about the recipe                 | String    | No       |
| `cookware`           | Cookware for the recipe                | String    | No       |
| `nutrition`          | Nutritional information of the recipe  | String    | No       |
| `favorite`           | Indicates if it's a favorite recipe    | Boolean   | No       |
| `rating`             | Recipe rating                          | Float     | No       |
| `categories`         | Recipe categories                      | [Category]| No       |
| `tags`               | Recipe tags                            | [Tag]     | No       |
| `lastModifiedDate`   | Last modification date of the recipe (YYYY-MM-DD HH:mm:ss) | String | No |


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
       "uuid":"dce2a77a-ff62-4a8c-a087-05d9300c6665",
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
