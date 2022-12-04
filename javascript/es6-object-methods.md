# ES6 Object Methods

We can use following syntax to create object methods in ES6.

```
const myObjectUpdatedToES6 = {
    value:100,
    getValue(){
        return this.value;
    },
    incrementValue(val){
        this.value = this.value + val;
        return this.value;
    }
}

```