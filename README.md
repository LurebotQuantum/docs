# Lurebot Quantum Docs

    .-----------------------.
    |.-----------.          |
    || Core -----|- Adapter | wrapper     Entity    := message part(s) e.g."[TEXT, IMG]"
    ||  |        |       |  |             Scripting :: Entity -> Entity
    '|--|--------|=======|=='             Core      :: Entity -(Scripting)-> Entity
     |  |        |       |                Adapter   :: a -(Core)-> a
     | Scripting |  IM (telegram, etc.)                where "a" is IM specific message
     '==========='
        quantum

- quantum: the core runner, should
  - keep _Core_ running
  - hotload custom _Scripting_ runner
- wrapper: manager and user interface, should
  - start/connect to _quantum_
  - manage adapters
  - be platform specific, has GUI, etc.

## License

[MIT License](https://opensource.org/licenses/MIT).