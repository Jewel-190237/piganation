# Pagination - React Pagination Component

A comprehensive React pagination component with search and dropdown functionality. Features customizable page sizes, search filtering, and responsive design.

## Features

- Pagination controls
- Search filtering
- Dropdown page size selection
- Customizable styling
- Responsive design
- Keyboard navigation
- Accessible interface

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Jewel-190237/piganation.git
   ```

2. Copy `piganation.tsx` and `global.css` into your project

3. Import and use the component:
   ```tsx
   import Pagination from './piganation';

   function App() {
     const data = Array.from({ length: 100 }, (_, i) => ({
       id: i + 1,
       name: `Item ${i + 1}`
     }));

     return (
       <Pagination
         data={data}
         itemsPerPage={10}
         renderItem={(item) => <div>{item.name}</div>}
       />
     );
   }
   ```

## Usage

### Basic Usage
```tsx
import Pagination from './piganation';

function App() {
  const items = Array.from({ length: 50 }, (_, i) => ({
    id: i + 1,
    name: `Product ${i + 1}`
  }));

  return (
    <Pagination
      data={items}
      itemsPerPage={10}
      renderItem={(item) => (
        <div key={item.id}>{item.name}</div>
      )}
    />
  );
}
```

### Custom Page Sizes
```tsx
<Pagination
  data={items}
  itemsPerPage={10}
  pageSizes={[5, 10, 20, 50]}
  renderItem={(item) => <div>{item.name}</div>}
/>
```

### With Search
```tsx
<Pagination
  data={items}
  itemsPerPage={10}
  searchable={true}
  searchKey="name"
  renderItem={(item) => <div>{item.name}</div>}
/>
```

## Props

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| data | array | [] | Array of items to paginate |
| itemsPerPage | number | 10 | Items per page |
| pageSizes | array | [5,10,20,50] | Page size options |
| searchable | boolean | false | Enable search filtering |
| searchKey | string | - | Key to search in objects |
| renderItem | function | - | Render function for items |

## Features in Detail

### Pagination Controls
- Previous/Next buttons
- Page number buttons
- First/Last page buttons
- Current page indicator

### Search Filtering
- Real-time search
- Filter by any property
- Clear search button

### Dropdown Selection
- Page size dropdown
- Custom page size options
- Responsive design

## Author

**Jewel-190237**
- GitHub: [Jewel-190237](https://github.com/Jewel-190237)
- Email: jewel190237@gmail.com

## Contributing

Feel free to fork this project and create pull requests for any improvements.

## License

This project is open source and available under the [MIT License](LICENSE).
