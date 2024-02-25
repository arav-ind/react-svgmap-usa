# React SVG Map USA

This package generates an interactive SVG map of USA. It allows users to highlight states on hover and retrieve the value of the selected state. The map includes all the states of USA.

![USA Map](./svgmap.gif)

## Installation

Install the package via npm:

```bash
npm install react-svgmap-usa
```

## State List

The following are the states mapped with its ID.

```js
const stateNames = {
  HI: 'Hawaii',
  AK: 'Alaska',
  FL: 'Florida',
  NH: 'New Hampshire',
  MI: 'Michigan',
  VT: 'Vermont',
  ME: 'Maine',
  RI: 'Rhode Island',
  NY: 'New York',
  PA: 'Pennsylvania',
  NJ: 'New Jersey',
  DE: 'Delaware',
  MD: 'Maryland',
  VA: 'Virginia',
  WV: 'West Virginia',
  OH: 'Ohio',
  IN: 'Indiana',
  IL: 'Illinois',
  CT: 'Connecticut',
  WI: 'Wisconsin',
  NC: 'North Carolina',
  DC: 'District of Columbia',
  MA: 'Massachusetts',
  TN: 'Tennessee',
  AR: 'Arkansas',
  MO: 'Missouri',
  GA: 'Georgia',
  SC: 'South Carolina',
  KY: 'Kentucky',
  AL: 'Alabama',
  LA: 'Louisiana',
  MS: 'Mississippi',
  IA: 'Iowa',
  MN: 'Minnesota',
  OK: 'Oklahoma',
  TX: 'Texas',
  NM: 'New Mexico',
  KS: 'Kansas',
  NE: 'Nebraska',
  SD: 'South Dakota',
  ND: 'North Dakota',
  WY: 'Wyoming',
  MT: 'Montana',
  CO: 'Colorado',
  ID: 'Idaho',
  UT: 'Utah',
  AZ: 'Arizona',
  NV: 'Nevada',
  OR: 'Oregon',
  WA: 'Washington',
  CA: 'California'
}
```

## Usage

```jsx
'use client'

import { useState } from 'react'
import USAMap from 'react-svgmap-usa'

export default function MapComponent() {
    const [state, setState] = useState('')

    return (
        <>
            <div>{state}</div>
            <USAMap
                onClick={(selectedValue: string) => setState(selectedValue)}
                size='500px'
                mapColor='white'
                strokeColor='#4f4f4f'
                strokeWidth='1'
                hoverColor='#3d3d3d'
            />
        </>
    )
}
```

## Props Available

| Props       | Description                                             | Requirement | Default Value |
|-------------|---------------------------------------------------------|-------------|---------------|
| onClick     | Callback function to get the selected state value.      | Required    | NA            |
| className   | Custom classname for the map component.                 | Optional    | "svgmap"      |
| size        | Width of the map.                                       | Optional    | "inherit"     |
| mapColor    | Color of the map.                                       | Optional    | "#ffffff"     |
| strokeColor | Border color of each state.                             | Optional    | "#000000"     |
| strokeWidth | Border width of each state.                             | Optional    | "0.5"         |
| hoverColor  | Color of the state while hovering on it.                | Optional    | "#303030"     |


## Contributing

Pull requests are welcome.

## Credits

Reference of SVG map taken from [MAPSVG](https://mapsvg.com/maps).