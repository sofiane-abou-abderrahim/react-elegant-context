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
