The core of the definition data model is the runtime graph. The purpose of this graph is to represent all definitions and their relationships in the runtime system. This is the primary data structure through which different parts of the system communicates.

We make some decisions about the structure of the graph:

* It is a runtime structure, so caching (and duplicating) data is acceptable as long as the cache data is known to the original source of the data (perhaps through a system that runs code).
* It is a typed graph, where the types are themselves placed into the graph.
* We use a naming standard for our graph types:
  * `NFooBar` is a node, and should be a noun phrase.
  * `EWantsFoo` is an edge, and should be a relationship.
  * `LFooBar` is a label, and should be a noun phrase.
  * `PFooBar` is a property, and should be a statement.

## Definitions

There are two crucial kinds of definitions: **types** and **subroutines**. These represent the core of any system, **types** are descriptions of objects (including subroutines), and **subroutines** are some sort of computation (in general something executable). Other nodes can be placed in the graph, but in general they will at least have either a type label or a subroutine label.

The first problem is bootstrapping the system. While the goal is to provide a generic data structure capable of representing any programming system, we must first be able to describe that data structure in an easy to access way. To do this we must describe an in memory representation. And then that in memory representation must describe itself.

### Objects

Here we add generic object features.

### Lifecycle

Here we add generic lifecycle features.

#### Meta Rules

The first set of generic features are those that manage the lifecycle of objects. For this we create some types in the runtime:

* `syn::core::LMetaRuleLifecycle` (`/Syndicate/Core/MetaRuleLifecycle`) this is a label for metatypes that effect the lifecycle of an object.

**Rule** an interpreter may only work with the memory of objects when the object's type node's type, object's type node's edge types, and object's type node's property types, that are in the label space `/Syndicate/Core/MetaRuleLifecycle` it has a complete understanding of.

#### InitialMemory

This is a property which tells any interpreting system that this type begins initalization by copying the memory contained in this property.

* `syn::core::graph::PInitialMemory` (`/Syndicate/Core/InitialMemory`) a node for a struct type (that is any type that takes up a chunk of memory). The value is a pointer for the memory to initalize with.

This leads to a computed property:

* `PlainOldData`: A type is "plain old data"

#### Constructor

#### Destructor
