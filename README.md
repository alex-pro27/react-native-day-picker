# react-native-day-picker

### it is a fork with https://github.com/ivanchenko/react-native-day-picker. Here we have added the ability to disable dates
 

## Getting Started

```sh
$ npm install https://github.com/great27/react-native-day-picker --save
```

## Example

```javascript

import React from 'react';
import {
    View,
    StyleSheet,
    AppRegistry
} from 'react-native';

import Calendar from './src/Calendar';


class DayPicker extends React.Component {
    render() {
        var from = new Date();
        from.setDate(from.getDate() - 16);
        var to = new Date();

        var startDate = new Date();
        startDate.setMonth(startDate.getMonth() + 1);

        return (
            <View style={styles.container}>
                <Calendar
                    monthsCount={24}
                    startFormMonday={true}
                    startDate={startDate}
                    selectFrom={from}
                    selectTo={to}
                    disabledDatesBackColor={'#E9E9EF'}
                    disabledDatesTextColor={'#808080'}
                    disabledDates={[
                        new Date('2018-01-05'), new Date('2018-01-15')
                    ]}
                    onSelectionChange={(current, previous) => {
                        console.log(current, previous);
                    }}
                />
            </View>
        );
    }
}

const styles = StyleSheet.create({
    container: {
        flex: 1,
        paddingTop: 20,
        justifyContent: 'center',
        alignItems: 'center',
        backgroundColor: '#F5F5F5'
    }
});
```
## Properties

All properties are optional

- **`onSelectionChange`** _(func)_ — Function which will be executed on day click. First param is clicked day date, second one previous clicked day.

- **`startDate`** _(Date)_ — Date from which you can select dates. By default is **new Date()**.

- **`width`** _(number)_ Calendars width, should be **divided on 7 without remainder** or may cause unpredictable behaviour.

- **`selectFrom`** _(Date)_ — First day in range that will be selected from start.

- **`selectTo`** _(Date)_ — Last day in range that will be selected from start.

- **`monthsCount`** _(number)_ — Count of dates from current months to the last.

- **`startFromMonday`** _(bool)_ — If true than months will started from monday.

- **`monthsLocale`** _(arrayOf(string))_ — Strings for localization, which will be displayed in month header started from January.

- **`weekDaysLocale`** _(arrayOf(string))_ — Strings for localization, which will be displayed in week day header, started from sunday.

- **`isFutureDate`** _(boolean)_ — True if you want to select a future date. By default is **false**.=======

- **`rangeSelect`** _(bool)_ — True if you want to select a range of dates. By default is true.

- **`disabledDates`** _(array[new Date()])_ - A list of dates which you want to disable


### Colors
 
- **`bodyBackColor`** _(string)_ — Calendar background color.

- **`bodyTextColor`** _(string)_ — Calendar headers text color.

- **`headerSepColor`** _(string)_ — Calendar header separator color.
 
- **`dayCommonBackColor`** _(string)_ — Not selected day background color.

- **`dayCommonTextColor`** _(string)_ — Not Selected day text color.
 
- **`dayDisabledBackColor`** _(string)_ — Disabled day background color.

- **`dayDisabledTextColor`** _(string)_ — Disabled day text color.
 
- **`daySelectedBackColor`** _(string)_ — First and last day in range background color.

- **`daySelectedTextColor`** _(string)_ — First and last day in range text color.
 
- **`dayInRangeBackColor`** _(string)_ — In range day background color.

- **`dayInRangeTextColor`** _(string)_ — In range day text color.

- **`monthTextColor`** _(string)_ — Calendar month header text color.

- **`disabledDatesBackColor`** _(string)_ In use disabled date background color

- **`disabledDatesTextColor`** _(string)_ In use disabled date text color

## Support

Email al.pro@mail.ru for support.
