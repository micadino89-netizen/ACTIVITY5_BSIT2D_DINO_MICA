#ANALYSIS

Why does the linked-list stack push at the head instead of the tail?
A singly linked list only has next pointers, so removing the tail means walking from the head to find the node before it, which makes pop O(n). At the head, both push and pop only change one reference (top), so each takes O(1) time. The head of the list therefore works naturally as the top of the stack.

Why must the array queue be circular?
In a plain array queue, each dequeue moves front forward and leaves unused slots at the start, so the queue runs out of space even though it isn't full. Shifting every element left after each dequeue would fix this but makes dequeue O(n). With the modulo operator, front and rear wrap around to index 0, so freed slots get reused and both enqueue and dequeue stay O(1).
