# Java 8 Using Optional to avoid NPE


** What is `Optional<T>`? **

an immutable container that can hold either a single non-null T reference or nothing at all (empty). An optional is essentially an immutable _collection_ that can hold at most one element, does not implement `Collection<T>` though.

** How do you create an `Optional<T>`? **

`Optional.empty()` - an empty value. Use it to communicate the absence of value.

`Optional.of(non-null-value)` - creates an optional containing the given non-null value. Use this only when you are 100% sure that value will always be non-null otherwise it will throw NPE. Avoid this.

`Optional.ofNullable(possibly-null-value)` - creates an optional containing the value if non-null, otherwise returns an empty optional. Always prefer this.

** How do you extract value from an `Optional<T>`? **

`Optional.get(someOptional)` - use this if you are 100% sure that `someOptional` is nonempty but if you are wrong it will throw `NoSuchElementException`. Avoid this.
