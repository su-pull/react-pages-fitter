# react-page-fitter

[![Release Status](https://img.shields.io/github/release/su-pull/react-page-fitter.svg)](https://github.com/su-pull/react-page-fitter/releases/latest)
![code size](https://img.shields.io/github/languages/code-size/su-pull/react-page-fitter)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

This is a React hook that observe HTML element fits within the current viewport.

## Installation

```sh
npm install react-page-fitter
```

## Usage

```tsx
import { useRef } from 'react'
import useFitter, { Main } from 'react-page-fitter'

function MyComponent() {
  const ref = useRef(null)
  const isFit = useFitter({ offsetY: 100, optional: ref })

  return (
    <Main classFitIn={style} classFitOut={style}>
      <div style={{isFit ? style : style}}> </div>
      {children}
    </Main>
  )
}
```

## API

useFitter({ref, options})

## Parameters

- ref (optional): RefObject to the HTML element to be observe.  
  If not set, observe the imported component.
- options (optional): viewport property values.

  1\. offsetX: A number representing the horizontal offset to use if the element fits. The default value is 0.

  2\. offsetY: A number representing the vertical offset to use if the element fits. The default value is 0.

## Tested

Next.js 13.2.4 Stable Pages Route  
Next.js 13.3.0 Beta App Route  
Remix 1.15.0 v2_routeConvention

## License

The MIT License.
