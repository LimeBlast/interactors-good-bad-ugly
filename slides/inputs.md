##  Inputs

    class SayHello < ActiveInteraction::Base
      string :name

      interface :serializer,
        methods: %i[dump load]

      object :cow # Cow class

      #...
    end

note:
    You start by defining your inputs, of which there are a large number of filters to choose from, including all the
    ones you'd expect such Strings, Arrays, Booleans, etc.. as well as the ability to define an input having a specific
    interface, or to be an instance of a particular class.
