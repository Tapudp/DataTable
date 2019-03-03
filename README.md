### A DataTable utility 
Shows all the headers in separate columns

### Sorting functionality
basically sorted on the basis of price,
that too with ascending and descending format, which changes upon clicking the button.

```js
sortBy(key) {
    this.setState({
      data: data.sort((a, b) => (
        this.state.direction[key] === 'asc'
          ? parseFloat(a[key]) - parseFloat(b[key])
          : parseFloat(b[key]) - parseFloat(a[key]))
      ),
      direction: {
        [key]: this.state.direction[key] === 'asc'
          ? 'desc'
          : 'asc'
      }
    })
  };
```