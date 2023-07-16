
A back-end connection to the front-end components, responsible for converting component data into a render friendly structure.

O3DE sets up processor instantiation separately from components. This means that processors have the ability to process multiple components at once.

What are the advantages to the O3DE method, and is there any reason that we should replicate this in our ECS system?

**Advantages**
- If the component functionality requires some awareness of the other components of the same type in the scene, then having a single processor makes this easier.
	- ex: collider component, if aware of all other collider components for free, then collision testing in processor becomes very easy.
- Some potential to re-use resources that are required for components
	- ex: some default icon texture which every component of same type requires.
**Disadvantages**
- More work, deciding where the processors need to be instantiated.
- Processors initialized may potentially be doing no work.