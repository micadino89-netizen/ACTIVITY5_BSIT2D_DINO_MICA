# Stacks and Queues: Array vs. Linked List

Implementations of a stack and a queue, each built two ways from first principles (no `list.insert(0, x)` or `pop(0)`).

## Files

| File | Description |
|---|---|
| `node.py` | `Node` class shared by the linked structures |
| `array_stack.py` | `ArrayStack`: fixed-size list, `top` starts at `-1` |
| `linked_stack.py` | `LinkedStack`: push/pop at the head, no capacity limit |
| `array_queue.py` | `ArrayQueue`: circular buffer using `front` + `size` |
| `linked_queue.py` | `LinkedQueue`: head (`front`) and tail (`rear`) references |
| `main.py` | Menu-driven program for all four implementations |
| `applications.py` | Balanced-parentheses checker (stack) and print-queue simulation (queue) |
| `test_driver.py` | Demo of all classes, including underflow, overflow and wrap-around |
| `sample_runs` | Output of the test driver and application exercise |
| `analysis.md` | Answer to the analysis question |

## How to run

Requires Python 3. Run all commands from this folder.

- **Menu program:** `python main.py`. Choose an implementation (ArrayStack, LinkedStack, ArrayQueue, LinkedQueue), enter a capacity for the array versions, then pick operations. The structure's state is printed after each operation.
- **Test driver:** `python test_driver.py`
- **Applications:** `python applications.py`

## Operations

| Structure | Operations |
|---|---|
| Stack | `push`, `pop`, `peek`, `is_empty`, `is_full` |
| Queue | `enqueue`, `dequeue`, `peek_front`, `is_empty`, `is_full` |

Underflow raises `IndexError` and overflow raises `OverflowError`, both with descriptive messages. The linked versions never overflow, so `is_full()` always returns `False`.
