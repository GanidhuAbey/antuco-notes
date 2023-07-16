Passes handle execution of the rendering pipeline, but what shaders specifically are executed is completely dependent on the object.

So we instead use pipelines to manage shaders, hence they need to be the link between the CPU side and GPU side resources.

Pipelines need to reflect the shader binding data, and offer methods to user of updating that data.

Pipelines can be per-object if necessary, so they are more specific than passes, which are merely just per output resource.