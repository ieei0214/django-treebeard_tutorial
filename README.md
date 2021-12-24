# django-treebeard

## Tutorial

https://django-treebeard.readthedocs.io/en/latest/tutorial.html

## Create some nodes
```
>>> from treebeard_tutorial.models import Category
>>> get = lambda node_id: Category.objects.get(pk=node_id)
>>> root = Category.add_root(name='Computer Hardware')
>>> node = get(root.pk).add_child(name='Memory')
>>> get(node.pk).add_sibling(name='Hard Drives')
<Category: Category: Hard Drives>
>>> get(node.pk).add_sibling(name='SSD')
<Category: Category: SSD>
>>> get(node.pk).add_child(name='Desktop Memory')
<Category: Category: Desktop Memory>
>>> get(node.pk).add_child(name='Laptop Memory')
<Category: Category: Laptop Memory>
>>> get(node.pk).add_child(name='Server Memory')
<Category: Category: Server Memory>
```

### example

![This is an image](example.jpg?raw=true)

