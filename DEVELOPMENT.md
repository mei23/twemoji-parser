
# Development

## How to update regex

[src/scala/README.md](src/scala/README.md) を見てScala環境を作る

src/scala/config/src/main/resources/config/emoji.yml をいい感じに編集する (別記予定)

`yarn generate`

`cp src/lib/regex.js dist/lib/regex.js`


## emoji.yml

```
  - unicode: "1f9b9-200d-2642-fe0f"
    description: "Man supervillain"
    keywords: "fantasy,bad,criminal,evil,superpowers,villain,man,male,men"
    type: "diversity"
```
基本は`unicode`にシーケンスを書く  
`description`, `keywords`は生成には影響しないけどなんか書いておく  
`type`はオプション  

### type

#### text-default

デフォルトでは、200dが含まれていない かつ 最後が fe0f で終わるシーケンスは、最後に fe0f が付いてなくても対象にする。  
このtypeにすると、該当絵文字は最後に fe0f が付いてないと対象にならなくなる。  
copyrightの絵文字等にこのフラグが付いている。
