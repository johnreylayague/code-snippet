
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

##

# React Typescript
