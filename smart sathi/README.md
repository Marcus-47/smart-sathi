# ParkEase — Parking Management System

A small, browser-only parking lot app. It uses plain HTML, CSS, and JavaScript, and stores all records in your browser’s local storage.

## Use it

Open `index.html` in any modern browser—there is nothing to install.

1. Use **Park** to enter a vehicle number and choose Bike or Car. Leave the slot choice on auto-assign or select a free slot.
2. Use **Dashboard** to see availability and click any slot to park or release a vehicle.
3. Use **Release** to search for a vehicle or select it from the currently parked list. Confirming release records the exit and shows a receipt.
4. Use **History** to search completed visits. Refreshing the page keeps the records on the same browser and device.

## Customize slots and prices

At the top of [script.js](script.js), change the `CONFIG` object:

```js
const CONFIG = {
  slots: ['A1', 'A2', 'A3'],
  rates: { Bike: 10, Car: 20 }
};
```

Add or remove slot labels in `slots`; update the numbers in `rates` to set hourly fees. Fees round up to a whole hour and always charge at least one hour.

To clear all demo or recorded data, clear this site’s browser storage (or run `localStorage.removeItem('parkease-data-v1')` from the browser developer console).
