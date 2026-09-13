# Java Development Tools - 4.42

A special thanks to everyone who [contributed to JDT](acknowledgements.md#java-development-tools) in this release!

<!--
---
## Java&trade; XX Support 
-->

---
## JUnit

### JUnit Test Run History Survives Restarts

<details>
<summary>Contributors</summary>

- [Carsten Hammer](https://github.com/carstenartur)
</details>

The `JUnit` view now preserves finished and stopped test runs when you close Eclipse normally and reopen the same workspace.
Recent runs reappear in the existing history,
up to the configured `Maximum count of remembered test runs`.
You can inspect previous results and failure traces after a restart without running the tests again.

Select a restored run to load its complete test tree and failure details on demand.
When the original saved launch configuration still exists,
you can also use `Rerun Test` and `Rerun Test - Failures First` after the restart.

### More Accurate JUnit Execution Times
<!-- https://github.com/eclipse-jdt/eclipse.jdt.ui/pull/3163 -->

<details>
<summary>Contributors</summary>

- [Carsten Hammer](https://github.com/carstenartur)
</details>

You can now see more accurate execution times in the `JUnit` view.
The updated test runner measures individual test durations directly in the test JVM using a monotonic clock,
avoiding communication delays and distortions caused by system-clock adjustments.

Select `Show Execution Time Details` from the view menu to display CPU time
and, when available, its user-mode and system portions and non-CPU elapsed time beside each test.
The new option is off by default and independent of `Show Execution Time`,
so you can display either, both, or neither.

CPU times describe only the measured test-execution thread, not worker threads started by the test.
Non-CPU time is elapsed time minus that thread's CPU time, not a separate measurement of waiting time.
CPU details appear only when the test JVM supports the measurement and the selected run contains the corresponding data.

Recorded timing details are retained with saved test runs,
so you can revisit them in the JUnit history even after restarting Eclipse.
Changing the display options does not change the recorded data.

<!--
---
## Java Editor
-->

<!--
---
## Java Views and Dialogs
-->

<!--
---
## Java Compiler
-->

<!--
---
## Java Formatter
-->

<!--
---
## Debug
-->

<!--
### JDT Developers
--> 
