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
const duration = new Duration(2, 30);
console.log(duration.totalMinutes); // 150
console.log(duration.totalHours); // 2.5

```
