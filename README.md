<div align="center">

<image src="http://m.qpic.cn/psc?/V51UyG6T2hLdbN0oEgHl3fEkH73KqJt7/TmEUgtj9EK6.7V8ajmQrEEsEylM*52lTktZHLze*PTbMCd2wg4o5kkEyKNVsVL9UM5xK4GLClF.TOL*ty*FnqAuxBQmobbAoJ.gYMo62EQY!/mnull&bo=wADAAAAAAAADByI!&rf=photolist&t=5" height="64"/>

# CSES

The Course Schedule Exchange Schema

**English** | [**中文简体**](./docs/cn/README.md)

</div>

## Introduction

CSES is a universal course schedule exchange schema that can be used for exchanging schedules between different software. It is designed to be simple and easy to use, and can be easily converted to other formats such as ClassIsland format.

## Features

- **Simple**: CSES is designed to be simple and easy to use.
- **Universal**: CSES is a universal format that can be easily converted to other formats.
- **Easy to use**: CSES is easy to use and can be easily understood by humans.

## Code Completion

You can enable code completion by importing the [Schema file] and configuring it as follows.

- [VS Ccode](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)
- [JetBrains](https://www.jetbrains.com/help/idea/yaml.html#use-schema-keyword)
- [Zed Editor](https://zed.dev/docs/languages/yaml#schemas)

[Schema file]: https://raw.githubusercontent.com/CSES-org/CSES/refs/heads/main/cses.schema.json

## Example

File Name: xxx.yml/xxx.yaml
Codec: UTF-8

```yaml
version: 1
subjects:
  - name: Math
    simplified_name: M # Optional, Better for Chinese subject name
    teacher: Mr. A # Optional
    room: 101 # Optional
  - name: English
    simplified_name: E
    teacher: Mr. B
    room: 102
  - name: Physics
    simplified_name: P
    teacher: Mr. C
    room: 103
  - name: Chemistry
    simplified_name: C
    teacher: Mr. D
    room: 104

schedules:
  - name: Monday
    enable_day: 1
    weeks: all
    classes:
      - subject: Math
        start_time: "08:00:00"
        end_time: "09:00:00"
      - subject: English
        start_time: "09:00:00"
        end_time: "10:00:00"
  - name: Tuesday-Odd
    enable_day: 2
    weeks: odd
    classes:
      - subject: Physics
        start_time: "08:00:00"
        end_time: "09:00:00"
      - subject: English
        start_time: "09:00:00"
        end_time: "10:00:00"
  - name: Tuesday-Even
    enable_day: 2
    weeks: even
    classes:
      - subject: Chemistry
        start_time: "08:00:00"
        end_time: "09:00:00"
      - subject: English
        start_time: "09:00:00"
        end_time: "10:00:00"
```

## License

[MIT](./LICENSE)

