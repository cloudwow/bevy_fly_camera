[![Crates.io](https://img.shields.io/crates/v/bevy_fly_camera)](https://crates.io/crates/bevy_fly_camera)

This is a really basic flying camera bundle and plugin for Bevy. It's useful for testing 3d games before you've coded your own movement system.

Keybinds can be edited, but the defaults are:

- W / A / S / D - Move along the horizontal plane
- Left Shift - Move downward
- Space - Move upward

# Example

```rust
use bevy::prelude::*;
use bevy_fly_camera::{FlyCamera, FlyCameraPlugin};

fn setup(mut commands: Commands) {
  commands
    .spawn(Camera3dComponents::default())
    .with(FlyCamera::default());
}

fn main() {
  App::build()
    .add_plugins(DefaultPlugins)
    .add_startup_system(setup.system())
    .add_plugin(FlyCameraPlugin)
    .run();
}
```

Check out the [simple example](examples/basic.rs)

---

If you like this crate, there are some [issues](https://github.com/mcpar-land/bevy_fly_camera/issues/7) that I would love to get some help on to make it more maintainable!

Any PRs are also welcome, though keep in mind that the project scope is intentionally tiny: A quick and dirty 3D motion camera, almost entirely intended for intermediate development steps or 3D demos.

---

# Version Matching

| Bevy Version | `bevy_fly_camera` Version |
| ------------ | ------------------------- |
| `0.1.0`      | `0.1.1`                   |
| `0.1.3`      | `0.3.0`                   |
| `0.2`        | `0.4.0`                   |
| `0.2.1`      | `0.4.1`                   |
| `0.3.0`      | `0.5.0`                   |
| `0.4.0`      | `0.6.0`                   |
