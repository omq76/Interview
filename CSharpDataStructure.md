





# Sorted List 

- Generic collection
- THe key has to implement the ```IComparable<T>``` interface

```cs
public class Animal : IComparable<Animal>
{
    public string Name { get; set; }

    public int CompareTo(Animal other)
        => this.Name.CompareTo(other.Name);
}
		
var sortedList = new SortedList<Animal, string>();
sortedList.Add(new Animal { Name = "Réglisse" }, "Beagle");
sortedList.Add(new Animal { Name = "Deamon" }, "Sharpei");
```

# The linked list

-Generic collection
