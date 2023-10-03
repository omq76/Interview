





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


```cs
var list = new LinkedList<Animal>();
var reglisse = new Animal { Name = "Reglisse" };
var reglisseNode = list.AddLast(reglisse);

var pluton = new Animal { Name = "Pluton" };
var plutonNode = list.AddFirst(pluton);

var hugo = new Animal { Name = "Hugo" };
var hugoNode = new LinkedListNode<Animal>(hugo);
list.AddAfter(plutonNode, hugoNode);

var node = list.First;
var NextNode = node?.Next;
```

