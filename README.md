# In this lecture I learn about How to make custom hooks and what is lazy loading ?

# Custom Hooks :
 - Hooks are reusable function given by react.When you have component logic that needs to be used by multiple components,we can extract logic to a custom hook

# Lazy loading : 
  - Lazy loading is a technique in React that allows you to load components, modules, or assets asynchronously, improving the loading time of your application. React provides a built-in React.lazy() method and Suspense component to achieve lazy loading.

    - Syntax for Lazy Loading:
    // Implement Lazy Loding with React.Lazy method
    const MyComponent = React.lazy(() => import('./MyComponent'));

# Steps to Implement Lazy Loading:
 - Recognize the component you want to Lazy Load.
  These are mostly Large or complex which is not necessary for all the users when the    page loads.
    Import the `lazy()` and Suspense components from the React package
    Use the `lazy()` function to dynamically import the component you want to lazy load:
    Note that the argument to the `lazy()` function should be a function that returns the result of the import() function. 
    Wrap the lazy-loaded component in a `Suspense` component, which will display a fallback UI while the component is being loaded:
    <Suspense fallback={<div>Loading...</div>}>
      <MyComponent />
    </Suspense>