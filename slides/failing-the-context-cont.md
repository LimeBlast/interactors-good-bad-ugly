##  Failing the Context cont.

    class SessionsController < ApplicationController
      def create
        result = AuthenticateUser.call(session_params)

        if result.success?
          session[:user_token] = result.token
          redirect_to root_path
        else
          flash.now[:message] = t(result.message)
          render :new
        end
      end
    end

note:
    Which will automatically trigger the result object to have .success? and .failure? booleans accordingly.
