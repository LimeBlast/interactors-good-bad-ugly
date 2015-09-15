##  Inputs cont.

    class SayHello < ActiveInteraction::Base
      string :name,
        default: 'World',
        desc: "Who you're saying hello to"

      #...
    end

note:
     And optionally, you've got the ability to set a default for each input, as well as a description which can be used
     to generate documentation.
