## Strategic Design

- ***Ubiquitous Language*** (Ngôn ngữ phổ biến):
  Everyone use the same terms, and those terms live in the code.
- ***Bounded Context***:
  A boundary within which a model is defined and consistent. The word "Order" might mean something different in the Billing context vs. the Shipping context.
  ![[Pasted image 20260517190739.png]]
- ***Context map***:
  A diagram showing how Bounded Contexts relate to each other.
## Tactical Design

- ***Entity***: an object with a unique identity that persists over time (e.g a User with ID)
- ***Value Object***: an immutable object defined by its attributes, not identity.
  A Value Object can contain a method/function to support it (e.g checking valid Email)
- ***Aggregate***: A group of entities/value objects treated as a single unit
- ***Aggregate Root***: The single entry point that guards that group.
```js
// ❌ Bad - outside code directly mutates a child
order.items.push(new OrderItem(productId, qty));

// ✅ Good - root controls all changes
order.addItem(productId, qty);
```
- ***Repository***: Stores and gets aggregates, doesn't care how it actually stores data.
  ex: userRepository
- ***Domain Service***: logic that doesn't belong to any single object.
  ex: transferring money between two accounts. It's not the job of Account A or Account B, it belongs to a TransferService
- ***Domain Event***: something that happened, written in past tense.
  ex: orderPlaced
- ***Factory***: 
### Anti-Corruption Layer (ACL)
- ACL is a boundary guard (renaming fields, converting types …)
- Turn external data into Value object, Aggregate, DTO