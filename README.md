# react-native-time-slot-picker
# demo
{/*
import React, { Component } from 'react';
import { Platform, StyleSheet, Text, View } from 'react-native';
import TimeSlotPicker from './src/TimeSlotPicker';

const platform = Platform.select({
  ios: 'IOS',
  android:
    'ANDROID',
});

export default class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      currentDate: new Date(),
      daySection: this.sections(),
      section: 12,
    }
  }


  tConvert(time) {
    // Check correct time format and split into components
    time = time.toString().match(/^([01]\d|2[0-3])(:)([0-5]\d)(:[0-5]\d)?$/) || [time];

    if (time.length > 1) { // If time format correct
      time = time.slice(1);  // Remove full string match value
      time[5] = +time[0] < 12 ? ' AM' : ' PM'; // Set AM/PM
      time[0] = +time[0] % 12 || 12; // Adjust hours
    }
    return time.join(''); // return adjusted time or original string
  }

  sections() {
    var section = 12;
    var daySection = [];
    var currentTime = 8;
    for (let i = 0; i < section; i++) {
      currentTime = currentTime + 1;
      formattedTime = this.tConvert(currentTime.toString() + ':00');
      avail = (i === 5 || i === 9 ? false : true);

      daySection.push({
        duration: 12, avail: i === 5 || i === 9 ? false : true, time: i === 0 ? formattedTime + ' AM' : formattedTime, minutes: [{ mm: 15, avail: i === 6 ? false : avail }, { mm: 30, avail: avail }, { mm: 45, avail: avail }, { mm: 60, avail: avail }]
      });

    }
    return daySection;
  }

  sections1() {
    var section = 14;
    var daySection = [];
    var currentTime = 8;
    var avail;
    for (let i = 0; i < section; i++) {
      currentTime = currentTime + 1;
      formattedTime = this.tConvert(currentTime.toString() + ':00');
      avail = (i === 5 || i === 9 ? false : true);
      daySection.push({ duration: section, avail: i === 5 || i === 9 ? false : true, time: i === 0 ? formattedTime + ' AM' : formattedTime, minutes: [{ mm: 15, avail: avail }, { mm: 30, avail: avail }, { mm: 45, avail: avail }, { mm: 60, avail: avail }] })
    }
    this.setState({ daySection: daySection, section: section });
  }

  render() {
    const { currentDate, section, daySection } = this.state;
    // var targetDate = new Date();
    // targetDate.setDate(targetDate.getDate() + 10);
    // setTimeout(() => { this.setState({ section: 10 }) }, 1000);

    return (
      <View style={styles.container}>
        <Text style={{ color: '#fff', fontSize: 20, alignSelf: 'center' }}>Time Slot Picker</Text>
        <TimeSlotPicker
          section={section}
          daySection={daySection}
          selectionBackGroundColor={'#29CFCA'}
          layoutColor={'#fff'}
          onDragSelect={(slot) => console.log('selected slot : ' + slot)} />
      </View >
    );
  }

}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    backgroundColor: '#484848'
  }
});
*/}