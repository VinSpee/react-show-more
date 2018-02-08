# Show More Items

## install

```
yarn add @tedconf/react-show-more
```

## use

[Here's a CodeSandbox demo](https://codesandbox.io/s/xjykw83n7z)

```jsx
import React from 'react';
import ShowMore from 'react-show-more';

const MyLongComponent = ({ listItems }) => (
  <ShowMore
    items={listItems}
    by={2}
  >
    {({
      current,
      onMore,
    }) => (
      <React.Fragment>
        <ul>
          {current.map(item => (
            <li
              key={item.id}
            >
              {item.label}
            </li>
          ))}
        </ul>
        <button
          disabled={!onMore}
          onClick={() => { if (!!onMore) onMore(); }}
        >
          more
        </button>
      </React.Fragment>
    )}
  </ShowMore>
);

render(
  <MyLongComponent
    listItems={[
      {
        id: '1',
        label: 'You can grow new brain cells. Here\'s how',
      },
      {
        id: '2',
        label: 'The brain may be able to repair itself — with help',
      },
      {
        id: '3',
        label: 'Growing evidence of brain plasticity',
      },
      {
        id: '4',
        label: 'One more reason to get a good night\'s sleep',
      },
    ]}
  />,
  yourEl,
);
```
