# Forth. Транслятор и модель

- Лабор Тимофей Владимирович P3225
- вариант: ```forth | stack | neum | mc | tick | binary | stream | port | pstr | prob2 | pipeline```
- выполнен без усложнения (pipeline)

## Язык программирования

### Синтаксис

```ebnf
program       = { statement , whitespace}
statement     = word
              | integer
              | comment
              | definition
              | base_word
              | loop
              | conditional
word          = { letter | digit }-
base_word     = "dup" 
              | "drop"
              | "swap"
              | "+" 
              | "-" 
              | "*" 
              | "/" 
              | "mod" 
              | "and" 
              | "or" 
              | "not" 
              | "=" 
              | ">" 
              | "<"
              | "store"
              | "load"
              | "print"
              | "input"
              | "variable"
              | "if ... else ... then"
              | "while"
integer       = [ "-" ] , { digit }-
comment       = "\" , { <any symbol except "\n"> } , "\n"
definition    = ":" , { whitespace }- , word , { statement , whitespace } , ";"
conditional   = "if" , { statement , whitespace }- [ "else" , { statement , whitespace }- ] , "then"
loop          = "begin" , { statement , whitespace} , "until" , { statement , whitespace }

name          = { letter | digit }-
whitespace    = " " | "\t" | "\n" | "\r"
digit         = <any of 0-9>
letter        = <any symbol>
```

### Семантика

Поддерживаются однострочные комментарии, начинающиеся с "\" 

Команды:

- `dup` --- продублировать вершину стека
- `drop` ---
- `swap` --- 
- `+` --- 
- `-` ---
- `*` ---
- `/` ---
- `mod`
- `and`
- `or`
- `not`
- `=`
- `>`
- `<`
- `store`
- `load`
- `print`
- `input`
- `variable`
- `if ... else ... then`

### Организация памяти


### Система команд


### Транслятор


### Модель процессора


### Тестирование
