This component extends all the props of **[Calendar](#calendar)** component. In addition to those props, it has the following props: 

| Prop Name  |  Type |
|---|---|
|  **moveRangeOnFirstSelection** |  boolean |
|  **retainEndDateOnFirstSelection** |  boolean |
|  **onRangeFocusChange** |  function |
|  **rangeColors**  |  array |
|  **ranges**  |  array |


#### Example: Empty view
The default range name when not providing a range is `range1`
```jsx inside Markdown
import {useState} from 'react'
const [state, setState] = useState([]);
  
<DateRange
  editableDateInputs={false}
  showDateDisplay={false}
  onChange={item => setState([item.range1])}
  moveRangeOnFirstSelection={false}
  ranges={state}
/>
```

#### Example: Editable Date Inputs
```jsx inside Markdown
import {useState} from 'react'
const [state, setState] = useState([
    {
      startDate: new Date(),
      endDate: null,
      key: 'selection'
    }
  ]);
  
<DateRange
  editableDateInputs={true}
  onChange={item => setState([item.selection])}
  moveRangeOnFirstSelection={false}
  ranges={state}
/>
```
