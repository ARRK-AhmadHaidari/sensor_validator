# Task: Implement a SensorValidator in C++

**Estimated time:** 1 hour  
**Build system:** Bazel  
**Test framework:** Google Test  
**Language standard:** C++17

---

## What you're building

A `SensorValidator` that checks whether a `SensorReading` is currently usable. A reading
fails if its value falls outside a configured range, or if it is older than a configured
maximum age. This kind of check is common inside safety-critical control loops in
automotive and robotics software.

The interface is fixed — implement it exactly as specified below. You write the `.cc`
implementation, the Bazel `BUILD` files, and the unit tests.

---

## Project layout

A basic framework with some provided files is given in this repo.

```

MODULE.bazel                    ← provided
BUILD.bazel                     ← root target file (can be empty for now)
lib/
 ├── BUILD.bazel                 ← you write this
 ├── sensor_validator.h          ← provided
 └── sensor_validator.cc         ← you implement this
test/
 ├── BUILD.bazel                 ← you write this
 └── sensor_validator_test.cc    ← you write this
```

---

## Requirements

- [ ] The library builds cleanly: `bazel build //lib:sensor_validator` succeeds
- [ ] All tests pass: `bazel test //...` exits with no failures
- [ ] At least **five meaningful tests** covering distinct scenarios
- [ ] No external dependencies beyond Google Test and the C++ standard library
- [ ] The header file is unchanged from the specification above

---

## Submitting your work

Host your solution in a public repository on a platform of your choice (GitHub, GitLab, Bitbucket, Codeberg, etc.) and share the link before the interview.

Treat the repository the same way you would in a production multi-developer project.

---

## Interview day — what to be ready to explain

During the interview you will walk through your own implementation. Be prepared
to answer questions like:

- What does each file in your project do, and why did you structure it this way?
- Why did you choose the tests you wrote? Do they cover all relevant test paths?

> There are no trick questions. The goal is to understand the code *you* wrote and
> the choices *you* made — not to recite theory.
