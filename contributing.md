# Contributing

lab-i is open source and contributions are welcome. You do not need to be an experienced developer to contribute — improving documentation, reporting bugs, and sharing feedback are all genuinely valuable.

---

## Ways to contribute

**Report a bug**  
Open an issue on the [GitHub repository](https://github.com/lab-intelligence/lab-i-app/issues). Include your platform (Android, Linux, Windows, macOS), what you expected to happen, and what actually happened. Screenshots help.

**Request a feature**  
Open an issue and describe what you need and why. The most useful feature requests come from actual research workflows — if something would genuinely save you time in the lab, it is worth raising.

**Improve the documentation**  
The docs live in the [lab-i-docs repository](https://github.com/lab-intelligence/lab-i-docs). If something is unclear, missing, or wrong, open a pull request with your changes. Documentation contributions are just markdown — no coding required.

**Contribute code**  
The app is built in Flutter. If you want to fix a bug or add a feature:

1. Fork the [lab-i-app repository](https://github.com/lab-intelligence/lab-i-app)
2. Create a branch for your change
3. Make your changes and test them on at least one platform
4. Open a pull request with a clear description of what you changed and why

---

## Development setup

You will need:
- Flutter (latest stable) — [flutter.dev](https://flutter.dev)
- An editor (VS Code with Flutter extension, Android Studio, or similar)
- Android SDK for Android builds
- For Linux builds: `cmake`, `ninja`, `clang`, `gtk3`, `pkg-config`

Clone the repo and run:
```bash
flutter pub get
flutter run -d linux   # or android, windows, macos
```

---

## Code style

- Follow standard Flutter and Dart conventions
- Keep changes focused — one fix or feature per pull request
- Test on at least one platform before submitting
- If your change affects the UI, include a screenshot in the pull request

---

## Licence

By contributing to lab-i you agree that your contributions will be licensed under the same MIT licence as the project.

---

## Questions

If you are not sure whether something is worth contributing or how to approach a change, open an issue and ask before investing a lot of time. It is better to discuss first than to build something that doesn't fit the project's direction.

Thank you for considering contributing to lab-i.
