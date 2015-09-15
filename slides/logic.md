##  Logic

    class SayHello < ActiveInteraction::Base
      string :name

      validates :name,
        presence: true

      def execute
        "Hello, #{name}!" # or: "Hello, #{inputs[:name]}!"
      end
    end

note:
    Then finally you perform the logic that's required inside an `execute` method. All the inputs defined are available
    as local variables, or as a hash named `inputs`.
