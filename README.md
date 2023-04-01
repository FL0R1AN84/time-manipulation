# TypeScript

``` typescript
class Duration {
  private _hours: number;
  private _minutes: number;

  constructor(hours: number, minutes: number) {
    this._hours = hours;
    this._minutes = minutes;
  }

  get hours(): number {
    return this._hours;
  }

  get minutes(): number {
    return this._minutes;
  }

  get totalMinutes(): number {
    return this._hours * 60 + this._minutes;
  }

  get totalHours(): number {
    return this._hours + this._minutes / 60;
  }
}

// Example usage
const duration = new Duration(6, 0);
console.log(duration.totalHours); // 6
console.log(duration.totalMinutes); // 360

const addPauseTimeInHours = duration.totalHours >= 6 ? duration.totalHours + .5 : duration.totalHours;
const addPauseTimeInMinutes = duration.totalMinutes >= 360 ? duration.totalMinutes + 30 : duration.totalMinutes;
console.log(addPauseTimeInHours); // 6.5
console.log(addPauseTimeInMinutes); // 390

```
