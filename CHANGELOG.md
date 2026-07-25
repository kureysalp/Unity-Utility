# Changelog

All notable changes to this package are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-07-25

### Added
- Initial release as a Unity Package Manager package.
- Extension methods for GameObject, Transform, Vector3, Rigidbody, Camera, string, List, IEnumerable, and numeric types.
- `Singleton<T>` and `PersistentSingleton<T>` MonoBehaviour base classes.
- `WaitFor` cached coroutine yield instructions.
- `VectorMath` static helpers.
- Optional `Unity.Mathematics` support via the `ENABLED_UNITY_MATHEMATICS` define.
