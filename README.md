# window-scroll

Here I want to the scroll window to top smoothly after user changes the page.

```js
import React from 'react';
import { Pagination } from 'antd';

const App = () => {
  const [query, setQuery] = useState('');

  const handleChange = async (page, take) => {
    await setQuery({
      ...query,
      page,
      take
    });
    
    window.scroll({
      top: 0,
      behavior: 'smooth'
    })
  } 

return (
  .
  .
  .
  <Pagination
    total={posts.pagination.totalCount}
    current={posts.pagination.page}
    showQuickJumper
    defaultPageSize={posts.pagination.take}
    showSizeChanger={false}
    onChange={handleChange}
  />
)

}
```
