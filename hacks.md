## Table of contents

1. [Key value pipe without changing the order of the keys  ](#key-value-pipe-with-keepOriginalOrder)



## key-value-pipe-with-keepOriginalOrder

By using 'keepOriginalOrder' along with the 'keyvalue' pipe.  The order of the keys is preserved.

eg:
```
<div *ngFor="let item of myObject | keyvalue: keepOriginalOrder">
  {{ item.key }} : {{ item.value }}
</div>
```
