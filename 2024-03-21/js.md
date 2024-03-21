```javascript
const obj = {
    Name: 'Greta',
    Nickname: 'Eco warrior',
    AKA: 'Captain Planet',
    Occupation: 'Unemployed',
}

const matchingResult = Object.fromEntries(
    Object.entries(obj).filter(([k, v]) => v.split(' ').length === 2)
)
const newObjModified = Object.fromEntries(
    Object.entries(obj).map(([k, v]) => [k, v.toUpperCase()])
)
```
