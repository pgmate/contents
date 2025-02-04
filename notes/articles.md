# Articles

Articles are stored in `contents/articles.json`.

> We know that this storage will not last forever, but damn... it will be good up to hundreds of items and we'll cross that bridge when we get to it.

### Article Item DTO

| requried | field   | type     | description                                          |
| :------: | ------- | -------- | ---------------------------------------------------- |
|    x     | id      | uuid     | unique ID for the entry                              |
|    x     | cdate   | time     | entry creation date                                  |
|    x     | media   | dict     | type of entry, will affect the template that is used |
|    x     | url     | url      | url to the resource                                  |
|    x     | title   | string   | display title                                        |
|          | cover   | url      | link to the cover image                              |
|          | excerpt | string   | display description                                  |
|    x     | tags    | string[] | list of associated tags                              |
|          | authors | text[]   | reference to the associated author                   |

### Author Item DTO

| requried | field | type | description                     |
| :------: | ----- | ---- | ------------------------------- |
|    x     | id    | text | unique ID for the entry         |
|    x     | name  | text | display name                    |
|          | bio   | text | short description of the author |
|          | url   | url  | link to the author's home page  |

### Tag Item DTO

| requried | field | type   | description                                      |
| :------: | ----- | ------ | ------------------------------------------------ |
|    x     | id    | text   | unique ID for the tag, used in the article's DTO |
|    x     | cover | url    | link to the cover of the tag                     |
|    x     | title | text   | display name                                     |
|          | desc  | string | display description                              |

### Supported Media

This field impacts the UX of the card that is presented in the app.

- `web` opens link in a new tab
- `reddit` opens up a link in a new tab, but can show a specific icon
- `youtube` plays video inline

### Tags

Tagging an entry is important because PGMate shows different lists of articles in the home page (product-updates, news, ...) with different styles.

Untagged products are only displayed in the "Articles" main page.
