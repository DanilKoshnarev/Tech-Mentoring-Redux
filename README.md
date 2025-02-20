# Управління Станом у Реактивних Додатках

Цей репозиторій роз'яснює основи управління станом у реактивних додатках на прикладі Redux і React.

## Зміст
1. Вступ до управління станом
2. Основи Redux
3. Дизайн Стану
4. Реалізація в React
5. Приклади коду
6. Література

## Вступ до управління станом
Управління станом є ключовим аспектом побудови складних інтерфейсів користувача в реактивних додатках.

## Основи Redux
Redux є популярною бібліотекою для управління станом, яка забезпечує передбачувані зміни стану.

## Дизайн Стану
Принципи дизайну стану, такі як єдина точка правди, незмінність даних та чисті функції.

## Реалізація в React
Інтеграція Redux з React для побудови реактивних додатків з передбачуваним управлінням станом.

## Приклади коду
### JavaScript (React)
```javascript
import { createStore } from 'redux';

// Reducer function
const reducer = (state = { count: 0 }, action) => {
    switch (action.type) {
        case 'INCREMENT':
            return { count: state.count + 1 };
        case 'DECREMENT':
            return { count: state.count - 1 };
        default:
            return state;
    }
};

// Create a Redux store
const store = createStore(reducer);

// Component
const Counter = () => {
    const count = useSelector(state => state.count);
    const dispatch = useDispatch();

    return (
        <div>
            <p>Count: {count}</p>
            <button onClick={() => dispatch({ type: 'INCREMENT' })}>Increment</button>
            <button onClick={() => dispatch({ type: 'DECREMENT' })}>Decrement</button>
        </div>
    );
};
```

## Література
1. *Redux: A Predictable State Container for JS Apps* by Dan Abramov and Andrew Clark
