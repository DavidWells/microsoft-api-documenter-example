<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [microsoft-api-documenter-example](./microsoft-api-documenter-example.md) &gt; [final](./microsoft-api-documenter-example.final.md)

## final() function

Function to make the provided constructor sealed and immutable

<b>Signature:</b>

```typescript
export declare function final(constructor: Function): void;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  constructor | Function | class definition to make immutable |

<b>Returns:</b>

void

## Remarks

This method is ment to be used as decorator. When this function is executed, it will seal both the constructor and its prototype which would not allow the class to be sub-classed at runtime, preventing new properties from being added to it and marking all existing properties as non-configurable. Values of present properties can still be changed as long as they are writable. Additionally, if this function is executed, it will freeze both the constructor and its prototype meaning that the object can no longer be changed. Freezing an object prevents new properties from being added to it, existing properties from being removed, prevents changing the enumerability, configurability, or writability of existing properties, and prevents the values of existing properties from being changed.

## Example


```typescript
\@final
class BugReport {
  title: string;

  constructor(t: string) {
    this.title = t
  }
}
```

