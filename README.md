# Flutter Counter App

This is a Flutter counter app that demonstrates state management using the `bloc` package. It leverages the power of `Cubit`, `BlocProvider`, and `BlocBuilder` to manage and build the UI based on the state.

## Features

- Increment and decrement counter functionality
- State management using `Cubit`
- Easy state handling with `BlocProvider` and `BlocBuilder`
- Clear separation of business logic and UI

## Getting Started

### Prerequisites

- Flutter SDK
- Dart SDK

### Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/ArslanYousaf12/bloc-counter.git
    ```

2. Navigate to the project directory:

    ```sh
    cd flutter-counter-app
    ```

3. Install the dependencies:

    ```sh
    flutter pub get
    ```

### Running the App

1. Run the app on an emulator or connected device:

    ```sh
    flutter run
    ```

## Usage

This app consists of a simple counter with increment and decrement buttons. The state of the counter is managed by a `CounterCubit`, which is provided to the widget tree using `BlocProvider`. The `BlocBuilder` listens for state changes and rebuilds the UI accordingly.

### Code Overview

#### CounterCubit

The `CounterCubit` handles the business logic of the counter. It extends `Cubit<CounterState>` and defines methods to increment and decrement the counter.

```dart
class CounterCubit extends Cubit<CounterState> {
  CounterCubit() : super(CounterState(counterValue: 0));

  void increment() => emit(CounterState(counterValue: state.counterValue + 1));
  void decrement() => emit(CounterState(counterValue: state.counterValue - 1));
}
