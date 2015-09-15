##  Running the interaction!

    SayHello.run!(name: nil)
    # ActiveInteraction::InvalidInteractionError: Name is required

    SayHello.run!(name: '')
    # ActiveInteraction::InvalidInteractionError: Name can't be blank

    SayHello.run!(name: 'Daniel')
    # => "Hello, Daniel!"

note:
    and .run! does away with the outcome object, and either raises an exception on failure, or simply returns the value
    on success.
