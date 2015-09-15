##  Inputs

    class SayHello < ActiveInteraction::Base
      string :name,
        default: 'World',
        desc: "Who you're saying hello to"

      #...
    end

note:
    You start by defining your inputs, of which there are a large number of filters to choose from, including all the
    ones you'd expect such Strings, Arrays, Booleans, etc.. as well as the ability to define an input having a specific
    interface, or to be an instance of a particular class. You've optionally got the ability to set a default, as well
    as a description which can be used to generate documentation.
