#### Note links
```dataview
list from [[]] and !outgoing([[]])
```
Fan-out is **the distribution of messages by a service or message router to multiple users, often simultaneously**.

---
# Domain Driven Design
## Strategic Design

- ***Ubiquitous Language*** (Ngôn ngữ phổ biến):
  Everyone use the same terms, and those terms live in the code.
- ***Bounded Context***:
  A boundary within which a model is defined and consistent. The word "Order" might mean something different in the Billing context vs. the Shipping context. 
- ***Context map***:
  A diagram showing how Bounded Contexts relate to each other.
## Tactical Design

- ***Entity***: an object with a unique identity that persists over time (e.g a User with ID)
- ***Value Object***: an immutable object defined by its attributes, not identity.
  An Value Object and contain 