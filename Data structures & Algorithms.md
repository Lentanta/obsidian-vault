# Tree Data Strucures
[[Tree Data Structures]]
## Tree Traversal
![[tree-search.webp]]
### Depth First Search
**In-Oder Traversal (DFS)**
Bottom -> Top
Left -> Root -> Right
```ts
function traverse(root) {
	traverse(root.left)
	print(root)
	traverse(root.right)	
}
```

**Pre-oder Traversal (DFS)**
Top -> Bottom
Root -> Left -> Right 
```ts
function traverse(root) {
	print(root)
	traverse(root.left)
	traverse(root.right)	
}
```

**Post-oder Traversal (DFS)**
Left -> Right -> Root
```ts
function traverse(root) {
	traverse(root.left)
	traverse(root.right)	
	print(root)
}
```
### Breadth First Search
Left -> Right
Top -> Bottom
```ts
queue = new Queue();
func traverse(root) {
	while(queue not empty) {
		// 1.Dequeue remove the head
		node = queue.dequeue()
		print(node)			

		// 2.Add node to queue and continue loop
		if(node.left != null) {
			queue.enqueue(node)
		}

		if(node.right != null) {
			queue.enqueue(node)
		}
	}
}
```
