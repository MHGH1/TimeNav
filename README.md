# Meeting Time Navigator

## Purpose

Meeting Time Navigator is a standalone HTML tool for planning meetings across multiple countries and time zones.

It is designed to answer a practical scheduling question:

> If a meeting is scheduled in one location, what date and time will it be elsewhere, and is that time reasonable for the other locations involved?

The tool combines:

- A visual world map with live local times.
- Time-zone conversion for proposed meetings.
- Working-hours impact indicators.
- Upcoming daylight-saving clock-change alerts.
- Public-holiday awareness.

This is particularly useful when coordinating meetings between Europe, North America, Asia and Australia, especially during periods when countries change their clocks on different dates.

## Included locations

The current version includes:

- UK, represented by London.
- Netherlands, represented by Amsterdam.
- Poland, represented by Warsaw.
- US East Coast, represented by New York.
- US West Coast, represented by Los Angeles.
- Pakistan, represented by Islamabad.
- Hong Kong.
- India, represented by Mumbai.
- Singapore.
- Japan, represented by Tokyo.
- Australia, represented by Sydney.
- UAE, represented by Dubai.

## How to open the tool

1. Download the HTML file to your computer.
2. Open the file in a modern web browser such as Microsoft Edge, Google Chrome or Firefox.
3. No installation is required.

The tool runs directly from the HTML file. An internet connection is required for live public-holiday data.

## How to use the tool

### 1. View live local times

The world map displays markers for the configured locations.

- Hover over a marker to see the location name, live local time and time-zone identifier.
- Click a marker to make that location the meeting reference location.
- Use the **24-hour / 12-hour** button in the top-right corner to change the displayed time format.

### 2. Choose a reference location

In the **Meeting planner**, select the location in which the meeting time is being proposed.

For example, selecting **Netherlands · Amsterdam** means the date and start time entered below will be interpreted as Amsterdam local time.

A reference location can be selected either:

- From the **Reference location** dropdown.
- By clicking its marker on the map.

### 3. Enter the meeting date

Enter the date in **DD/MM/YYYY** format.

Example:

```text
25/09/2026
```

The date must:

- Be a valid calendar date.
- Use a four-digit year.
- Fall between 2020 and 2100.

Use the **Today** button to reset the field to the current date.

### 4. Select the meeting start time

Select the local start time using the separate hour and minute fields.

Minutes are available in 15-minute intervals:

- 00
- 15
- 30
- 45

The quick-adjustment buttons can be used to:

- Move the meeting **15 minutes earlier**.
- Set the meeting to the **current time** in the reference location.
- Move the meeting **15 minutes later**.

### 5. Select the duration

Choose the planned meeting duration:

- 30 minutes.
- 60 minutes.
- 90 minutes.

The duration is currently recorded as part of the meeting proposal but does not change the working-hours classification, which is based on the meeting start time.

### 6. Review the global impact

The planner immediately converts the selected meeting into the local date and time for every configured location.

Each location is classified as:

- **Preferred:** the meeting starts between 09:00 and 17:29 local time.
- **Extended hours:** the meeting starts between 07:00 and 08:59, or between 17:30 and 19:59 local time.
- **Unsociable:** the meeting starts before 07:00 or from 20:00 onwards.

The summary beneath the location list shows how many locations fall into each category.

### 7. Review upcoming alerts

The **Upcoming alerts** section contains:

- **Clock changes:** the next detected daylight-saving or offset change across the configured locations.
- **Upcoming public holidays:** the next public holiday returned for the configured countries.

These alerts are intended to draw attention to dates when normal time-zone relationships or local availability may differ.

### 8. Review the detailed comparison

The **Meeting impact by location** table shows:

- Location and time zone.
- Local meeting date.
- Local meeting time.
- UTC offset on the selected date.
- Working-hours impact.
- Public-holiday status.

Use this table as the final detailed check before proposing a global meeting time.

## Known limitations

### Calendar availability is not checked

The tool does not connect to Outlook, Microsoft Teams or another calendar service. It cannot determine whether a person or meeting room is actually available.

### It does not create or send meetings

Meeting Time Navigator is a planning aid only. It does not create calendar invitations, send notifications or reserve rooms.

### Working-hours rules are fixed

The current working-hours classifications are built into the tool and cannot be customised by location or user.

The classifications are based only on the meeting start time. They do not assess whether the meeting ends outside working hours.

### Duration has limited impact

Selecting a duration does not currently alter the impact assessment. A meeting beginning at 17:00 is classified from its 17:00 start even if a 90-minute meeting would continue into extended hours.

### Public-holiday data depends on an external service

Holiday information is loaded from an external public-holiday API when the file opens.

Holiday information may be unavailable if:

- The device is offline.
- The API cannot be reached.
- The browser blocks the request.
- The external data source does not contain the relevant holiday.

### Public holidays may not cover every local variation

The holiday check is country-based. Regional, state, provincial, municipal, company-specific and optional holidays may not be represented consistently.

A displayed holiday should be treated as a prompt to verify local arrangements rather than definitive confirmation that every person in that country is unavailable.

### Clock-change alerts show the next detected change

The alert highlights the next detected time-zone offset change among the configured locations. It does not currently provide a full calendar of every future transition or explain every temporary difference between pairs of locations.

### Location coverage is predefined

The included locations are fixed in the HTML. There is currently no interface for adding, removing or reordering locations.

Each displayed city is used as the representative time zone for its named area. This may not reflect every time zone or daylight-saving rule within a larger country.

### Internet time is not independently synchronised

Live clocks use the device's current date and time, converted through the browser's time-zone data. If the device clock is incorrect, the displayed times may also be incorrect.

### Browser time-zone data may vary

Time-zone and daylight-saving calculations rely on the browser and operating system. An outdated browser or operating system may contain outdated time-zone rules.

### The file is standalone

Preferences and proposed meeting details are not saved between sessions. Closing or refreshing the file returns the tool to its default state.

## Recommended use

Meeting Time Navigator should be used to identify a sensible candidate meeting time and flag potential time-zone, clock-change or holiday issues.

Before confirming an important meeting:

1. Review the working-hours impact across all relevant locations.
2. Check any clock-change or public-holiday warning.
3. Confirm attendee availability in the organisation's calendar system.
4. Verify local holidays or special working arrangements where necessary.
