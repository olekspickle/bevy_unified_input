# bevy_unified_input

Ever wanted to bind multiple inputs at a time? A unified input primitives is just the thing

WIP: the api is still kinda cumbersome, but I found it useful for libraries that need some default bindings

# Example

```rust,no_run

use bevy::prelude::*;
use bevy_unified_input::*;

#[derive(Resource)]
struct MyInput {
speed_up_timeline: InputBinding,
slow_down_timeline: InputBinding,
}

impl Default for MyInput {
    fn default() -> Self {
        Self {
            speed_up_timeline: [KeyCode::KeyX.into(), GamepadButton::DPadRight.into()].into(),
            slow_down_timeline: [KeyCode::KeyZ.into(), GamepadButton::DPadLeft.into()].into(),
        }
    }
}
```

Full example see [`bevy_top_down_camera`](https://github.com/olekspickle/bevy_top_down_camera) examples.

## Bevy Version Compatibility

| bevy | bevy_unified_input   |
| ---- | -------------------- |
| 0.19 | 0.3.0                |
| 0.18 | 0.1.0-0.2.*          |


## License

Licensed under either of

 * Apache License, Version 2.0
   ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license
   ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.
