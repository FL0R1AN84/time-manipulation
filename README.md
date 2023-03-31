# Day.js

``` typescript
import dayjs from 'dayjs';

function getDuration(start: Date, end: Date): string {
  const duration = dayjs(end).diff(dayjs(start), 'minute');
  const hours = Math.floor(duration / 60);
  const minutes = hours >= 6 ? + 30 : duration % 60;

  return `${hours}h ${minutes}min`;
}

// Example usage
const start = new Date();
const end = new Date(Date.now() + (6 *60* 60 * 1000));
console.log(getDuration(start, end));
```
