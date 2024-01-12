
# Typescript
#### Interface Combined Types

```javascript
interface Type1 {
  name: string;
}

interface Type2 {
  age: number;
}

interface CombinedType1 extends Type1, Type2 {}

type CombinedType2 = Type1 & Type2;

const combinedData1: CombinedType1 = {
  name: "John Doe",
  age: 2,
};
const combinedData2: CombinedType2 = {
  name: "John Doe",
  age: 2,
};
```


#### Casting

```javascript
const requiest = req.name as string;
```

#### Generics

```javascript

// Example #1

const generic = <T>(data: T, other: number): T => {
  return data;
};

generic<string>("sd", 0); // const generic: <string>(data: string, other: number) => string

// Example #2

interface IGeneric<T> {
  data: T;
  other: number;
}

const GenericData = <T>(arg: IGeneric<T>): T => {
  return arg.data;
};

type TType = { name: string; age: number };

GenericData<TType>({ data: { name: "bossRod", age: 25 }, other: 0 }); //const GenericData: <TType>(arg: IGeneric<TType>) => TType
```

##

# React Typescript

#### React.FC

```javascript
import classes from "./TodoItem.module.css";

const TodoItem: React.FC<{ text: string; onRemoveTodo: () => void }> = (
  props
) => {
  return (
    <li className={classes.item} onClick={props.onRemoveTodo}>
      {props.text}
    </li>
  );
};

export default TodoItem;
```
