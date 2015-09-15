##  Context

    class SayHello
      include Interactor

      def call
        context.hello = "Hello, #{context.name}!"
      end
    end

    result = SayHello.call({name: 'Daniel'})
    result.hello
    # => "Hello, Daniel!"

note:
    The most important aspect of Interactor is the context, which gets created from the values you pass in, and
    manipulated accordingly by the business logic contained within. Unlike active_interactor, you don't define specific
    inputs, so if you have specific input or validation requirements, you'll need to establish them elsewhere.
