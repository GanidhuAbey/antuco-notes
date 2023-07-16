
Current memory allocator is inadequate, most of the effort is put on the user in providing the correct data.

currently, we don't have a memory allocator but instead an independent set of abstractions for different memory types. We need to form a further abstraction on top of this, that will actually handle the create and destruction of different memory types, i.e. an actual memory allocator.

A singleton pattern seems best for this.