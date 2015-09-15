##  Validation

    class SayHello < ActiveInteraction::Base
      string :name

      validates :name,
        presence: true

      #...
    end

note:
    Next, if you want some more control over the data which gets input, you've got the ability to set some  able to use
    ActiveModel validations. These are entirely optional.
