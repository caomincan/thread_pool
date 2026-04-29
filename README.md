# ThreadPool

A simple C++11 Thread Pool implementation.

Based on [progschj/ThreadPool](https://github.com/progschj/ThreadPool) (MIT License).

## Basic usage

```c++
// create thread pool with 4 worker threads
ThreadPool pool(4);

// enqueue and store future
auto result = pool.enqueue([](int answer) { return answer; }, 42);

// get result from future
std::cout << result.get() << std::endl;
```

## Build

```bash
g++ -std=c++11 -o example example.cpp -pthread
./example
```
