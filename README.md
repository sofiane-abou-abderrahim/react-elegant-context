# Advanced State Management

## Beyond Basic Apps & "Lifting Up State"

- The Problem of Shared State: Prop Drilling
- Embracing Component Composition
- Sharing State with Context
- Managing Complex State with Reducers

# Steps

## 0. Understanding Prop Drilling & Project Overview

1. run `npm install`
2. run `npm run dev`
3. create `README.md`

## 1. Prop Drilling: Component Composition as a Solution

1. embrace component composition by refactoring the `Shop.jsx` component to a wrapper around the list of products
2. output the `<Product />` component inside the `<Shop>` component in `App.jsx`

## 2. Creating & Providing The Context

1. create a `store` folder
2. create a `shopping-cart-context.jsx` file
3. inside of this file, create a `CartContext` context
4. provide it to this application and wrap it around the components in `App.jsx` by using `<CartContext.Provider>`

# 3. Consuming the Context

1. consume the `CartContext` in the `Cart.jsx` component
   1. import `{ CartContext }`
   2. import `{ useContext }`
   3. set `useContext(CartContext)` as a value to `cartCtx`
   4. use `cartCtx` to access the `items` property
2. add a value to `<CartContext.Provider>` in `App.jsx`
3. destructure `CartContext` so that you use `{ items }` straight away

## 4. Linking the Context to State

1. set the value of `<CartContext.Provider>` to the `shoppingCart` state in `App.jsx` to link the context to state
2. to edit the state with context, create a `ctxValue` const which will be an object
3. use `CartContext` in `Product.jsx`
4. add `addItemToCart` function as an initial value in `shopping-cart-context.jsx` file

## 5. A Different Way Of Consuming Context

1. use the `<CartContext.Consumer>` component to wrap the JSX code in `Cart.jsx`
2. pass a function as a child inside `<CartContext.Consumer>` to automatically receive the consumed `cartCtx` value as a parameter

## 6. Migrating the Entire Demo Project to use the Context API

1. remove extra props
2. use `CartContext` in `Header.jsx`
3. add the `updateItemQuantity` function in the `ctxValue` constant in `App.jsx` & in `shopping-cart-context.jsx`
4. extract `updateItemQuantity` in `Cart.jsx` & call it on the buttons

## 7. Outsourcing Context & State Into a Separate Provider Component

1. export a `CartContextProvider` function in `shopping-cart-context.jsx`
2. import `CartContextProvider` & use it in `App.jsx`
