# Tree Data Strucures
---
[[Tree Data Structures]]
## Tree Traversal
![[1_7oIYbZPNlSSwS4qnz-Di6g.webp]]

**In-Oder Traversal (DFS)** 
Left -> Root -> Right
```ts
function traverse(root) {
	traverse(root.left)
	print(root)
	traverse(root.right)	
}
```

**Pre-oder Traversal (DFS)**
Root -> Left -> Right 
```ts
function traverse(root) {
	print(root)
	traverse(root.left)
	traverse(root.right)	
}
```

**Post-oder traversal (DFS)**
Left -> Right -> Root
```ts
function traverse(root) {
	traverse(root.left)
	traverse(root.right)	
	print(root)
}
```



