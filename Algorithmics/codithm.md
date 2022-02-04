
*** _Codithm Universal Language Specification_ ***

**Author**:        _Aesth
**Description** :  *A paper/editor compatible descriptive language for thinking code and constructing design patterns.*
**Note** :         Use Fira Code font to show the ligatures.

    All Rights Reserved.


# Operators
-> . : :: ( ) [ ] { } < >

    -> flow descriptor
    :  structure | type descriptor 

    .  structure accessor
    :: namespace accessor

    ( ) value container
    [ ] type container 
    { } structure container
    < > propagation container

## Flow Descriptor (->)
*Code is nothing but the ochestrated motion of data.*
    
    -> pull data 
    <- push data

### Value Container (( ))
*Values can either be refered to directly or be evaluated from expressions.*

*To isolate evaluations and group our expressions, we employ parenthesis.*

    (expression)
    
### Data Translation
*Declaring and mutating a variable.*

    variable <- value | expression

*Referencing a variable.*

    reference -> variable

*Interacting with resource.*

    stream | file <- value | expression
    stream | file -> variable

*Exposing data through an interface.*

    <- value | expression 
    -> value | expression 

### Data Rotation+Scaling 
*Defining a function.*

    function <-
        ->
        instructions

    function <-
        ->
        instructions
    <---returns

    function <- arguments
        ->
        instructions

    function <- arguments
        ->
        instructions
    <---returns

*Calling a function.*

    -> function

    parameters -> function 

### Execution Control
*__If__-statement.*

    condition
        ->
        instructions
    ->
        instructions

*__While__-statement.*

    condition
        ()
        instructions

_**Break**- and **Continue**-statement in-use._

    condition
        ()
        instructions
    <---stop | skip

*__For__-statement.*

    variable <- <initial -> final>
        ()
        instructions

    element <- <list>
        ()
        instructions

    Object.<initial -> .mutate -> final>
        ()
        instructions

*__Switch__-statement*

    variable | expression
        -> value
            ->
            instructions
    <-------stop
        ...
        -> value
            ->
            instructions

        ->
        instructions

    Object.state
        -> description
            ->
            instruction
        ...

## Structure|Type Descriptor (:)
*Data just like water must adopt the shape of what it represents.*

    data : structure | type

### Type Container ([ ])
*Structures and types can be primitive, composite or derivative*

    [ type <- primitive | composite | derivative ]

    composite : {
        property : type
        ...
    }

    derivative : type -> {
        ...
    }

    variable : [ type ]

### Structure Container ({ })
*The design of patterns recognizes various interpretations of a structure.*

    { code | associations | namespace | object }  

    code : {

        instructions

    }

    associations : {

        .key <- value
        ...

    }


    namespace : {

        ::property
        ::feature

    }

    object : {

        .state <- [ properties ]
        .accessors <- [ setters getters ]
        .mutators <- [ transformations ]
        .constructor

    }

*The instruction for __pass__ are empty braces.*
    {}  


