## Thu Le

CS & Math @ Drexel. I build low-latency systems in C++ and the backends around them.

Most of my work starts the same way: something is slower or less correct than it should be,
and I want to know exactly why. Usually the answer is a cache line, a lock, or a number
nobody checked.

### Things I've built

**[Custom Memory Allocator](https://github.com/imbaothu/my-allocator)** · C++17, CMake  
Three-phase object-pool allocator — free list → pooled slabs → per-thread slab ownership —
to kill mutex contention in multithreaded trading systems. **3× the throughput of glibc
malloc at 4 concurrent threads.**

**[Lock-Free SPSC Queue](https://github.com/imbaothu/Lock-free-queue)** · C++17  
Single-producer/single-consumer queue built on cache-line padding and acquire/release
atomics. **34× lower p50 and 131× lower p999 latency** than a mutex-based baseline.

**Equity Research & Backtesting Platform** · Python, FastAPI, PostgreSQL, Redis, C++17  
Market data ingestion → factor scoring → point-in-time backtesting, with a C++ engine
cross-validated against an independent Python reference implementation. Caught a drawdown
calculation that reported a 50% loss as no loss at all.

### Currently

Going deeper on memory models, lock-free data structures, and where latency actually hides
in a system. Interested in quant infrastructure and anything performance-critical.

📫 lebaothu678@gmail.com

