# in-memory-entity-index-search

A basic in-memory implementation to index and search upon classes - "entities." Entities are converted into JSONDocument and inserted into a dictionary value-field-entity. Entities are assumed to have a unique Id field.

```
public class TestObject
{
    public string Id { get; set; }
    public string Name { get; set; }
    public int Age { get; set; }
}
```

This can be indexed into a format similar to:

```
{
    "12345": {
        "id": [Entity]
    },
    "John": {
        "name": [Entity]
    },
    "18": {
        "age": [Entity]
    }
}
```

This has support for any number of nested objects and will store those values in a "dot-notation" - firstlevel.nested. 