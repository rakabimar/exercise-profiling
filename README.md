# Modul 5: Java Profiling
### Tutorial Advanced Programming 2024/2025

- Name    : Rakabima Ghaniendra Rusdianto
- NPM     : 2306228472
- Class   : Pemrograman Lanjut A

## Reflection on Performance Testing and Profiling
### 1. Difference Between Performance Testing with JMeter and Profiling with IntelliJ Profiler
Performance testing with JMeter focuses on simulating multiple user requests to analyze an application's behavior under load, measuring metrics like response time, throughput, and error rates. On the other hand, profiling with IntelliJ Profiler provides deep insights into the application's internal performance, such as CPU usage, memory allocation, and method execution times. JMeter helps identify performance bottlenecks at a system level, while IntelliJ Profiler pinpoints inefficient code at a granular level.

### 2. How Profiling Helps Identify Weak Points
Profiling helps in identifying inefficient methods, excessive memory usage, and CPU-heavy operations. By analyzing execution time, memory allocation patterns, and thread activity, it highlights the specific code segments causing performance degradation. This insight allows developers to focus optimization efforts on the most critical performance bottlenecks.

### 3. Effectiveness of IntelliJ Profiler
IntelliJ Profiler is highly effective in detecting bottlenecks as it provides real-time analysis of CPU and memory usage. It allows developers to trace method execution, identify redundant computations, and find memory leaks. The detailed breakdown of resource consumption helps in making informed optimization decisions.

### 4. Challenges in Performance Testing and Profiling
One of the main challenges is reproducing real-world conditions in a controlled test environment. Performance issues may not always be consistent, making it difficult to pinpoint the root cause. Another challenge is interpreting profiling data, as large applications can generate overwhelming amounts of information. These challenges can be overcome by carefully designing test scenarios, using baseline comparisons, and focusing on critical execution paths.

### 5. Benefits of Using IntelliJ Profiler
- Provides real-time insights into CPU and memory usage.
- Helps identify inefficient loops, recursive calls, and unnecessary object creation.
- Aids in detecting memory leaks and garbage collection issues.
- Enables developers to measure the impact of optimization changes instantly.

### 6. Handling Inconsistencies Between IntelliJ Profiler and JMeter
When profiling results differ from JMeter findings, it is crucial to analyze both test environments. Factors such as test data, workload distribution, and caching mechanisms can cause discrepancies. To address this, cross-check results using different profiling tools and perform repeated tests under controlled conditions.

### 7. Strategies for Optimizing Application Code
After analyzing profiling and performance testing results, I implement optimizations such as:
- Reducing redundant computations and optimizing algorithms.
- Using caching mechanisms to reduce database queries.
- Enhancing concurrency to improve multi-threaded performance.
- Minimizing memory allocations to prevent excessive garbage collection.

## JMeter Reports and Test Results
### **Endpoint** `/all-students`
- **JMeter Report (CLI)**
  <img src="/src/img/jmeter-all-students-cli.png">
- **JMeter Report (GUI), Before Optimization**
  <img src="/src/img/jmeter-all-students-before.png">
- **JMeter Report (GUI), After Optimization**
  <img src="/src/img/jmeter-all-students-after.png">
- Improvements by Optimizing `getAllStudentWithCourses()`:

  | Before | After  | Diff Percentage |
    |--------|--------| -- |
  | 44956 ms | 5327 ms | 88.1% |

### **Endpoint** `/all-students-name`
- **JMeter Report (CLI)**
  <img src="/src/img/jmeter-all-students-name-cli.png">
- **JMeter Report (GUI), Before Optimization**
  <img src="/src/img/jmeter-all-students-name-before.png">
- **JMeter Report (GUI), After Optimization**
  <img src="/src/img/jmeter-all-students-name-after.png">
- Improvements by Optimizing `joinStudentNames()`:

  | Before | After  | Diff Percentage |
    |--------|--------| -- |
  | 1808 ms | 124 ms | 93.1% |

### **Endpoint** `/highest-gpa`
- **JMeter Report (CLI)**
  <img src="/src/img/jmeter-highest-gpa-cli.png">
- **JMeter Report (GUI), Before Optimization**
  <img src="/src/img/jmeter-highest-gpa-before.png">
- **JMeter Report (GUI), After Optimization**
  <img src="/src/img/jmeter-highest-gpa-after.png">
- Improvements by Optimizing `findStudentWithHighestGpa()`:

  | Before | After  | Diff Percentage |
      |--------|--------| -- |
  | 1808 ms | 124 ms | 93.1% |


