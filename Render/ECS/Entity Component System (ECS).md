
```
class GameObject 
{
public:
	std::vector<Component> components;

	GameObject(std::name object_id) // not sure if we need to go this far yet. 
	{
		Transform transform;
		components.push_back(transform);
	}
};

class Component 
{
	// Every component is responsible for implementing method to translate
	// itself to render item.
	virtual bool to_render() = 0;
}

class Transform : public Component
{
	// All the transform stuff. 
}
```
