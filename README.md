# vira_test

A useful, production-ready utility package for the **Vira Programming Language**.

## Features Included
- **Vec2 Geometry**: 2D floating-point vector math (add, sub, scale, dot).
- **Math Utilities**: Numerical functions (clamp, min_int, max_int).
- **Structured Logger**: Tagged, counter-tracked console logger (info, ok, warn, error).

## Installation

Add this package to any Vira project with the Vira Package Manager:

### From GitHub:
```bash
vira add github.com/<your-username>/vira_test
```

### From Local Path:
```bash
vira add C:/Users/hp/vira_test
```

## Usage Example

```vira
module my_app

import "vira_test"

fn main() {
    mut log := Logger.new('App')
    log.info('Initializing 2D physics engine...')

    pos := Vec2.new(10.0, 20.0)
    vel := Vec2.new(2.5, -1.0)
    new_pos := pos.add(vel)

    log.ok('Updated position: (${new_pos.x}, ${new_pos.y})')

    bounded_speed := clamp(120, 0, 100)
    println('Bounded speed: ${bounded_speed}')
}
```

## Running Tests

```bash
vira test tests/
```

## Publishing to GitHub

1. Create a new repository named 'vira_test' on GitHub.
2. In this directory, run:
```bash
git init
git add .
git commit -m "feat: initial release of vira_test package"
git branch -M main
git remote add origin https://github.com/<your-username>/vira_test.git
git push -u origin main
```
