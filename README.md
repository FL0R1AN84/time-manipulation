# Moment.js

``` typescript
import moment from 'moment';

function getDuration(start: Date, end: Date): string {
  const duration = moment.duration(moment(end).diff(moment(start)));
  const hours = duration.hours();
  const minutes = duration.hours() >= 6 ? + 30 : duration.minutes();

  return `${hours}h ${minutes}min`;
}

// Example usage
const start = new Date();
const end = new Date(Date.now() + (6 * 60 * 60 * 1000));
console.log(getDuration(start, end));
```
