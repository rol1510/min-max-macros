# min-max-macros
`no_std` crate for macros to get the minimum and maximum. 

## Install
```toml
min-max-macros = "0.1.0"
```

## Usage
```rust
use min_max_macros::{max, min};

let result = min!(1, -2);
assert_eq!(result, -2);

/* Works with everything that supports the < and > operators */
let result = max!(1.2, 4.4);
assert_eq!(result, 4.4);

let result = max!((1, 8), (1, 2));
assert_eq!(result, (1, 8));

/* Works with any number of arguments */
let result = max!(1, 2, 3, 4, 5, 6, 7);
assert_eq!(result, 7);

let result = max!(1);
assert_eq!(result, 1);
```