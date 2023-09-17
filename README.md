# Eat n Split is a React App

This app was built as an optional challenge for [The Ultimate React Course](https://www.udemy.com/course/the-ultimate-react-course/) taught by Jonas Schmedtmann. The app showcases using React Hooks to update State.

## Things I learned

- When I need an unique id in a new object I usually use `date()` but this time I used `crypto.randomUUID()`. This generated a very long randomw alph-numeric string. Only down side is that it will not work on older browsers. For this project it is okay but not for anything truly for the public.

- Used a avatar generating api to get the friends' images. In the `image: "https://i.pravatar.cc/48?u=499476"` element the number 48 calls for an image with the size of 48 units. The ?u=499476 will assign an id to the avatar so that it can be re-loaded each time the url is called in the browser. In this app the friend's id is used for the url's id as well. When a fried is added the image element string looks like this, `image:${image}?=${id}`

- Made use of optional chaining which is a vanilla JS concept to keep the initial state of the selectedFriend `null`. Without optional chaining `?` a `null` value will break everything in logic that needs a real value. For example the isSelected variable logic won't work if selectedFriend is `null`. So you need to add a `?` and then this `const isSelected = selectedFriend?.id === friend.id` will work beautifully.

## Useful Resources

- [crypto.randomUUID()](https://developer.mozilla.org/en-US/docs/Web/API/Crypto/randomUUID)
- [Avatar API](https://i.pravatar.cc/48)
- [Optional Chaining](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Optional_chaining)

### Notes about Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh
