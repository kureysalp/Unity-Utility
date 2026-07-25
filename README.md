# Unity Utility

A lightweight collection of Unity utility classes — extension methods, singleton base classes, coroutine helpers, and vector math — packaged for the Unity Package Manager.

Everything lives under a single namespace:

```csharp
using UnityUtils;
```

## Installation

### Package Manager (git URL)

1. Open **Window → Package Manager**.
2. Click **+ → Add package from git URL…**
3. Enter:

   ```
   https://github.com/kureysalp/Unity-Utility.git
   ```

### manifest.json

Alternatively, add the dependency directly to `Packages/manifest.json`:

```json
{
  "dependencies": {
    "com.kureysalp.unity-utility": "https://github.com/kureysalp/Unity-Utility.git"
  }
}
```

**Requires Unity 2021.3 or newer.**

## What's included

### Extensions
Fluent extension methods for the types you touch every day:

- **GameObject / Transform** — `GetOrAdd`, `OrNull`, hierarchy paths, recursive layer setting, child enable/disable/destroy, pose get/set, and more.
- **Vector3** — component-wise `With` / `Add` / `ComponentDivide`, range checks, random offsets, points in an annulus, grid quantization.
- **Rigidbody** — redirect velocity while preserving speed, stop instantly (Unity 6 `linearVelocity` aware).
- **Camera** — viewport extents with margin for frustum culling.
- **String** — null/blank checks, slicing, alphanumeric conversion, and rich-text formatting helpers.
- **List / IEnumerable** — `Shuffle`, `Swap`, `Filter`, `Clone`, `ForEach`, and allocation-aware `Random` selection.
- **Numbers / Mathf** — `Remap`, `AtLeast` / `AtMost` clamping, odd/even checks, approximate comparison, and `Min` / `Max` for extra numeric types.

### Singletons
Base classes for MonoBehaviour singletons:

- **`Singleton<T>`** — auto-instantiating, scene-scoped singleton.
- **`PersistentSingleton<T>`** — survives scene loads via `DontDestroyOnLoad`, with optional auto-unparenting.

### Coroutine helpers
- **`WaitFor`** — cached `WaitForSeconds` / `WaitForFixedUpdate` / `WaitForEndOfFrame` instructions to cut per-frame GC allocations in coroutines.

### Math
- **`VectorMath`** — static helpers for signed angles on a plane, dot-product projection, projecting points onto lines, rotating vectors onto planes, and more.

## Optional dependency

If the [**Unity.Mathematics**](https://docs.unity3d.com/Packages/com.unity.mathematics@latest) package is present, extra `half`-typed overloads in the numeric helpers are enabled automatically through the `ENABLED_UNITY_MATHEMATICS` define — no configuration required.

## License

Released under the MIT License. See [LICENSE](LICENSE).
