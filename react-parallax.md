# React Tilt

[![npm version][npm-badge]][npm-url]
[![npm downloads][downloads-badge]][npm-url]
[![npm bundle size][size-badge]][npm-url]
[![CI][build-badge]][build-url]
[![Codecov Coverage][coverage-badge]][coverage-url]
[![semantic-release][semantic-badge]][semantic-url]
[![prettier][prettier-badge]][prettier-url]
[![TypeScript][typescript-badge]][typescript-url]

_👀 Easily apply tilt hover effect on React components_

![](demo.gif)

## [Demo 💥](https://mkosir.github.io/react-parallax-tilt)

## Install

```bash
npm install react-parallax-tilt
```

## Features

- Lightweight (3.8kB), zero dependencies 📦
- Supports **mouse** and **touch** events
- Support for device tilting (**gyroscope**)
- **Glare** effect 🌟 with custom props (color, position,...) [🔗demo](https://mkosir.github.io/react-parallax-tilt/?path=/story/react-parallax-tilt--parallax-effect-glare-scale)
- Events to keep track of component values 📐 (tilt, glare, mousemove,...) [🔗demo](https://mkosir.github.io/react-parallax-tilt/?path=/story/react-parallax-tilt--events-all)
- Many effects and functionalities that can be easily applied:
  - **scale** on hover [🔗demo](https://mkosir.github.io/react-parallax-tilt/?path=/story/react-parallax-tilt--scale)
  - **disable** x/y axis [🔗demo](https://mkosir.github.io/react-parallax-tilt/?path=/story/react-parallax-tilt--tilt-disable-axis)
  - **flip** component vertically/horizontally [🔗demo](https://mkosir.github.io/react-parallax-tilt/?path=/story/react-parallax-tilt--flip-vh)
  - tilt hover effect on the **whole window** [🔗demo](https://mkosir.github.io/react-parallax-tilt/?path=/story/react-parallax-tilt--track-on-window)
  - tilt component with custom **manual input** 🕹 (joystick, slider etc.) [🔗demo](https://mkosir.github.io/react-parallax-tilt/?path=/story/react-parallax-tilt--tilt-manual-input)
  - **parallax** effect on overlaid images [🔗demo](https://mkosir.github.io/react-parallax-tilt/?path=/story/react-parallax-tilt--parallax-effect-img)

## Example

```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Tilt from 'react-parallax-tilt';

const App = () => {
  return (
    <Tilt>
      <div style={{ height: '300px', backgroundColor: 'darkgreen' }}>
        <h1>React Parallax Tilt 👀</h1>
      </div>
    </Tilt>
  );
};

ReactDOM.render(<App />, document.getElementById('root'));
```

## Props

All of the props are optional.  
Below is the complete list of possible props and their options:

> ▶︎ indicates the default value if there's one

**glareReverse**: _boolean_ ▶︎ `false`  
Reverse the glare direction.

**scale**: _number_ ▶︎ `1`  
Scale of the component (1.5 = 150%, 2 = 200%, etc.).

**perspective**: _number_ ▶︎ `1000`  
The perspective property defines how far the object (wrapped/child component) is away from the user. The lower the more extreme the tilt gets.

**transitionSpeed**: _number_ ▶︎ `400`  
Speed of the transition when manipulating the component.

**trackOnWindow**: _boolean_ ▶︎ `false`  
Track mouse and touch events on the whole window.

**gyroscope**: _boolean_ ▶︎ `false`  
Boolean to enable/disable device orientation detection.



## Gyroscope - Device Orientation

Please keep in mind that detecting device orientation is currently [experimental technology](https://developer.mozilla.org/en-US/docs/MDN/Contribute/Guidelines/Conventions_definitions#Experimental).  
Check the [browser compatibility](https://caniuse.com/#search=DeviceOrientation) before using this in production.  
A few takeaways when using device orientation event:

- always use secure origins (such as `https`)
- it doesn't work in all browsers when using it in cross-origin `<iframe>` element

<details>
<summary>Using device orientation on iOS 13+</summary>

Apple decided turning device motion and orientation off by default since iOS 12.2.  
With iOS 13+ permission API can be used to gain access to device orientation event.

When using gyroscope feature:

```jsx
<Tilt gyroscope={true}>
  <h1>React Parallax Tilt 👀</h1>
</Tilt>
```

it will present a permission dialog prompting the user to allow motion and orientation access at domain level:
![](device_orientation.jpg)

Note that user needs to take some action (like tapping a button) to be able to display the dialog (invoking dialog on page load is not possible).

</details>

## Development

_Easily set up a local development environment!_

Build all the examples and start storybook server on [localhost:9009](http://localhost:9009):

- clone
- `npm install`
- `npm start`

**Start coding!** 🎉

<details>
<summary>Or setup with npm link</summary>
Clone this repo on your machine, navigate to its location in the terminal and run:

```bash
npm install
npm link # link your local repo to your global packages
npm run build:watch # build the files and watch for changes
```

Clone project repo that you wish to test with react-parallax-tilt library and run:

```bash
npm install
npm link react-parallax-tilt # link your local copy into this project's node_modules
npm start
```

</details>

## Contributing

All contributions are welcome!  
Please take a moment to review guidelines [PR](.github/pull_request_template.md) | [Issues](https://github.com/mkosir/react-parallax-tilt/issues/new/choose)

[npm-url]: https://www.npmjs.com/package/react-parallax-tilt
[npm-badge]: https://img.shields.io/npm/v/react-parallax-tilt.svg
[typescript-badge]: https://badges.frapsoft.com/typescript/code/typescript.svg?v=101
[typescript-url]: https://github.com/microsoft/TypeScript
[prettier-badge]: https://img.shields.io/badge/code_style-prettier-ff69b4.svg
[prettier-url]: https://github.com/prettier/prettier