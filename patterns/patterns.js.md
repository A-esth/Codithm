# Error Handling
```javascript

function wrapper(arg){
    try{

        return wrapped(arg)

    } catch (error){

        // using error to adjust the behavior
        return wrapper(arg)

    }
}

```

# Comprehension List
```javascript

const list = [
    ...(()=>{

        // complex logic that generates a list 

        return generated

    })()
]


```