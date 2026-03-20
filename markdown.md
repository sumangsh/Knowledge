# hello
## This is my first markdown

**Good way of writing documents**

> This is blockquote

*this is italics*
1. First item
2. Second item
3. Third item

```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

```mermaid
graph TD;
  A-->B;
  A-->C;
  B-->D;
  C-->D;
```

| code  | color                                           |
| :---- |:------------------------------------------------|
| #0F0  | <span style="color:rgb(0,200,0)">&#9724;</span> |
| #F00  | <span style="color:rgb(200,0,0)">&#9724;</span> |

```sequence
Alice->Blob
```

```mermaid
graph LR
    fa:fa-check-->fa:fa-coffee
```
```plantuml
@startuml
Bob -[#red]> Alice : hello
Alice -[#0000FF]->Bob : ok
@enduml
```

```mermaid
stateDiagram
    [*] --> First
    state First {
        [*] --> second
        second --> [*]
    }
```


```mermaid
erDiagram
  customer }|..|{ Delivery-Address : has
```

```mermaid
architecture-beta
service db(database)[Database] in db_rg
```


- [ ] cdcld 
