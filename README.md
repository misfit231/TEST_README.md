# TEST_README.md
Here is a detailed README for the test cases:

# Flappy Bird Test Cases

This README provides information on the resources and justification for developing test cases for the Flappy Bird game implementation in Python.

## Resources Used

The following resources were used to create effective test cases:

- **unittest** - The unittest framework in Python provides useful base classes, assertions, mocks and tools for testing Python code. Using unittest allowed creating test case classes, setup/teardown and organizing tests.

- **Mocking** - To isolate code under test from external dependencies like Pygame, mocking is used to simulate function calls and test side effects. pygame.sprite.Group.empty and mouse events are mocked to test game reset and button click handling.

- **Pygame** - Pygame is initialized in setup and quit in teardown to allow testing Pygame specific behavior like sprite positions.

- **Assertions** - unittest assertions like assertEqual are used to check expected vs actual results in tests for game state, scores etc.

## Justification

- Using **unittest** over raw asserts provides organization of test cases and initialization/cleanup ability.

- **Mocking** pygame, mouse and time isolates the code under test from unpredictible side effects. Makes tests deterministic.

- Testing Pygame specific behavior requires initializing it in **setUp**. quit in tearDown cleans it up.

- **Assertions** from unittest make tests readable and clear on expected vs actual results.

## Other Information

- Tests chosen check core game behavior like scoring, game over handling, sprite state.

- Test class and method names follow conventions for clarity.

- Comments explain the purpose of tests 

- Tests are written to work independently to catch isolated bugs.

- More tests could be added for edge cases and different game states.
