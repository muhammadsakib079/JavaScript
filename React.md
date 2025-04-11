# 📘 React `fetch()` API Guide

This document provides a complete guide to using the `fetch()` method in React, including:

- ✅ Basic usage
- ✅ Using `useState` and `useEffect`
- ✅ Error handling
- ✅ Best practices
- ✅ Async/await version
- ✅ Custom hook bonus

---

## 1. 📌 Basic Syntax

```jsx
useEffect(() => {
  fetch('https://api.example.com/data')
    .then((response) => response.json())
    .then((data) => {
      console.log(data);
      // Do something with the data
    })
    .catch((error) => {
      console.error('Error fetching data:', error);
    });
}, []);
```

### 🔍 Explanation

| Part | Description |
|------|-------------|
| `useEffect(() => { ... }, [])` | React Hook that runs the fetch only once after component mounts. |
| `fetch('url')` | JavaScript function to make HTTP requests. |
| `.then(response => response.json())` | Converts the response to JSON. |
| `.then(data => {...})` | Handles the actual JSON data. |
| `.catch(error => {...})` | Catches and logs errors (e.g., network issues). |

---

## 2. ⚙️ Using `useState` with `fetch()`

```jsx
import React, { useEffect, useState } from 'react';

function MyComponent() {
  const [data, setData] = useState([]);
  const [loading, setLoading] = useState(true);

  useEffect(() => {
    fetch('https://api.example.com/items')
      .then((res) => res.json())
      .then((json) => {
        setData(json);
        setLoading(false);
      })
      .catch((err) => {
        console.error(err);
        setLoading(false);
      });
  }, []);

  return (
    <div>
      {loading ? <p>Loading...</p> : (
        <ul>
          {data.map(item => <li key={item.id}>{item.name}</li>)}
        </ul>
      )}
    </div>
  );
}
```

### 🔍 What's Happening Here

| State | Purpose |
|-------|---------|
| `data` | Stores the fetched JSON data. |
| `loading` | Controls loading state UI. |

✅ `useEffect` is perfect for side effects like API calls.  
✅ `useState` stores and updates data for rendering.

---

## 3. 🧼 Async/Await Version (Cleaner)

```jsx
useEffect(() => {
  const fetchData = async () => {
    try {
      const res = await fetch('https://api.example.com/data');
      const json = await res.json();
      setData(json);
    } catch (err) {
      console.error('Fetch error:', err);
    } finally {
      setLoading(false);
    }
  };

  fetchData();
}, []);
```

### ✅ Advantages

- Cleaner syntax with `async/await`
- Easier error handling with `try...catch`
- `finally` ensures loading state updates

---

## 4. 💡 Best Practices

| Practice | Why? |
|---------|------|
| Always handle loading and error states | Better UX and debugging |
| Use `async/await` for cleaner syntax | Readability and maintainability |
| Store API URLs in `.env` | Security and configuration |
| Add `key` when rendering lists | Prevent React warning and improve rendering |
| Create custom hooks for reusable fetch logic | DRY (Don't Repeat Yourself) code |

---

## 5. 📦 Bonus: Custom Hook Example

```jsx
import { useState, useEffect } from 'react';

export function useFetch(url) {
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);

  useEffect(() => {
    const getData = async () => {
      try {
        const res = await fetch(url);
        if (!res.ok) throw new Error('Network response was not ok');
        const json = await res.json();
        setData(json);
      } catch (err) {
        setError(err.message);
      } finally {
        setLoading(false);
      }
    };

    getData();
  }, [url]);

  return { data, loading, error };
}
```

### 🧠 Usage Example

```jsx
import React from 'react';
import { useFetch } from './useFetch';

function Posts() {
  const { data, loading, error } = useFetch('https://api.example.com/posts');

  if (loading) return <p>Loading...</p>;
  if (error) return <p>Error: {error}</p>;

  return (
    <ul>
      {data.map((post) => (
        <li key={post.id}>{post.title}</li>
      ))}
    </ul>
  );
}
```

---

## 🏁 Conclusion

React's `fetch()` API is simple and powerful for getting data into your components.  
With `useEffect`, `useState`, and optionally `async/await`, you can fetch and display data easily and cleanly.

> 💡 Want to make it even more reusable? Use custom hooks and environment variables for better project structure.

---

