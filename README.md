# play-data

extended relational data management tool for games

- enum definition: 
    - defines in csv 

- table schema definition: 
    - columns with types
    - primitive types:
        - number types : u8, i8, u16, i16, u32, i32, u64, i64, fload, double 
        - string: string 
        - enum: 
    - vec: [T] where T is a primitive type
    - map: <T, S> where T and S are primitive type
    - generic field 
        - T: v where T is a primitive type and v is its value.
    - unique index 
    - primary key 
    - foreign key 

- example values: 
    - primitive types are simple. 
        - 32u8, 1.01f, 3.02
        - "name" 
        - EnumType.EnumValue
    - composite type 
        - vec: [1, 2, 3] of [u32], ["a", "b", "c"] of [string] 
        - map: [(1, "a"), (2, "b")] of <u32, string>
    - generic field
        - u8: 3 
        - EnumCharacterType: Hunter 

- table space to manage schemas and enums: 
    - matches the namespace of C++

- code generation 
  - c++ generator 
  - naming convention option 
  - index accessor per table
  - foreign key validation on load
  - automatic reload and reuse elements pointer 
