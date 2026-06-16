## Table of contents

1. [Key value pipe without changing the order of the keys  ](#key-value-pipe-with-keepOriginalOrder)
2. [*ngIf and display:none difference](#*ngIf-and-display:none-difference)



## key-value-pipe-with-keepOriginalOrder

By using 'keepOriginalOrder' along with the 'keyvalue' pipe.  The order of the keys is preserved.

eg:
```
<div *ngFor="let item of myObject | keyvalue: keepOriginalOrder">
  {{ item.key }} : {{ item.value }}
</div>
```
## *ngIf-and-display:none-difference
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
