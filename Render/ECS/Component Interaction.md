Components add behaviour to entities, but sometimes these behaviours are dependent on other behaviours. 

For example a collision component needs to know where the entity is in order to calculate collisions. So it's dependent on the transform component.

Easy way to handle this is to store all components in a lookup table using a singleton class. That way we can quickly access any component from anywhere, provided we have the id of the original entity.