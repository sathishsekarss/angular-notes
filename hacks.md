## Table of contents

1. [Key value pipe without changing the order of the keys](#key-value-pipe-with-keepOriginalOrder)
2. [ngIf and display none difference](#ngIf-and-display-none-difference)
3. [Difference between forkJoin and combineLatest](#difference-between-forkJoin-and-combine-latest)

## key-value-pipe-with-keepOriginalOrder

By using 'keepOriginalOrder' along with the 'keyvalue' pipe.  The order of the keys is preserved.

eg:
```
<div *ngFor="let item of myObject | keyvalue: keepOriginalOrder">
  {{ item.key }} : {{ item.value }}
</div>
```
## ngIf-and-display-none-difference
| Feature | `*ngIf` | `display: none` |
|----------|----------|----------|
| DOM Element | Removed from DOM | Remains in DOM |
| Component Lifecycle | Created and Destroyed | Stays Alive |
| Memory Usage | Frees resources when removed | Still consumes memory |
| Event Listeners | Removed | Still attached |
| Change Detection | Not run for removed component | Still runs |
| Performance | Better for large/expensive components | Better for frequent show/hide |
| Component State | Lost when recreated | Preserved |
| Access via DevTools | Not visible in DOM | Visible in DOM |
| Initial Render Cost | Recreated each time condition becomes true | Rendered once |
| Best Use Case | Expensive components, conditional rendering | Frequent toggling, preserving state |

## difference-between-forkJoin-and-combine-latest

| Feature | `forkJoin` | `combineLatest` |
|----------|------------|----------------|
| When does it emit? | After **all observables complete** | Whenever **any observable emits** (after all have emitted at least once) |
| Number of emissions | Usually **one** | **Multiple** |
| Requires completion? | Yes | No |
| Best use case | Multiple HTTP API calls | Combining live data streams |
| Emits latest values? | Only final values | Always latest values |
| If one observable never completes | Never emits | Works normally |
| Similar to | `Promise.all()` | Reactive data synchronization |
| Works well with HTTP calls? | ✅ Yes | ⚠️ Yes, but usually unnecessary |
| Reacts to future changes? | ❌ No | ✅ Yes |
| Waits for all sources to emit at least once? | Yes (and complete) | Yes |
| Common Angular use cases | Loading multiple APIs on page load | Forms, filters, search, UI state synchronization |

Quick Memory Trick to remember:

| Operator | Think Of |
|----------|----------|
| `forkJoin` | "Wait for everyone to finish, then give me the result once." |
| `combineLatest` | "Keep me updated whenever anything changes." |
