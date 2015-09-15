##  Failing the Context

    class AuthenticateUser
      include Interactor

      def call
        if user = User.authenticate(context.email, context.password)
          context.user = user
          context.token = user.secret_token
        else
          context.fail!(message: "authenticate_user.failure")
        end
      end
    end

note:
    When something goes wrong in your interactor, you can flag the context as failed....
