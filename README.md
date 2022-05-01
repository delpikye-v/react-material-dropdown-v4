<div align="center">
    <h1>react-material-dropdown-v4z</h1>
    <br />
    <a href="https://codesandbox.io/s/gl1vu0">LIVE EXAMPLE</a>
</div>

---

#### Description
+ React simple dropdown / menu.
+ Can limit option or auto fit window height.
+ Auto change orientation if height exceeds window. (checking...)
+ Show tooltip if need. (text overflow)
+ <b>Single select.</b>
---

#### Usage
```js
npm install react-material-dropdown-v4z react-material-tc-i4z
```

Import the module in the place you want to use:
```js
import "react-material-tc-i4z/dist/styles.css"; // require for tooltip if need (text-overflow: ellipsis)

import BasicDropDown from 'react-material-dropdown-v4z'
```

#### Snippet

##### `simple`

```js
    const [value, setValue] = useState(null)

    <BasicDropDown
        width="300px"
        placeholder="abcd"
        // noDataText="this is nodata"
        disabledValues={[2]}
        // maxHeightDropdown="10px" // it display depend min
        // maxDisplay={2}
        // vertical="top"
        options={opt}
        // disabled={true}
        keyName="key"
        labelName="label"
        tooltipLabel={{
          placement: "top",
          // enabled: true
          // className ...
        }}
        tooltipItem={{
          placement: "right",
          //  enabled: true
          // className ...
        }}
        selectedValue={value}
        onSelection={(item) => setValue(item.key)}
      />
      {value}

      // const opt = [
      //     { key: 1, label: "21323 232323j2lk3jl2j"},
      //     { key: 2, label: "22"},
      //     { key: 3, label: "23"},
      //     { key: 4, label: "24"},
      //     { key: 5, label: "25"},
      //     { key: 7, label: "26"},
      //     { key: 8, label: "27"},
      //     { key: 9, label: "28"},
      //   ]

    //  const opt = [1, 2, 3, 4, 5, 6]
    //  const opt = ["1", "2", "3", "4", "5", "6"]

```
#### props
```js
id?                | string           |
name?              | string           |
style?             | CSSProperties;   |
className?         | string;          |
menuClassName?     | string;          |
placeholder?       | string           |
noDataText?:       | string           | text when no data
selectedValue?:    | string, number,  |
options:           | array[];         | list options [same type]
disabledValues?:   | array[];         | disabled list value
keyName?:          | string;          | if option is obj.
labelName?:        | string;          | if option is obj.
width?:            | string, number   |
height?:           | string, number   |
paddingTransform?: | string, number   | padding transform
maxHeightDropdown  | string, number   | maxHeight list
vertical?:         | top, bottom      | only support. (// TODO LEFT RIGHT)
autoDirection?:    | true             | auto change top/left
                                      |    if height > screen
maxDisplay?:       | number;          | limit option
minDisplay?:       | number;          | min option
tooltipLabel?:     | IDropDownTooltip | config tooltip for label
tooltipItem?:      | IDropDownTooltip | config tooltip for item
onSelection?:      | func             |
```

<br />

```js
IDropDownTooltip from 'react-material-tc-i4z'

always?: boolean;        | always tooltip
enabled?: boolean;       |
...

```
#### NOTE
You should add class to customize the color.

#### RUN

<a href="https://codesandbox.io/s/gl1vu0">LIVE EXAMPLE</a>

```js
npm install
```
```js
npm run dev
npm run start
```

### License

MIT
