##  Forms

    # GET /accounts/new
    def new
      @account = CreateAccount.new
    end

    # POST /accounts
    def create
      outcome = CreateAccount.run(params.fetch(:account, {}))

      if outcome.valid?
        redirect_to(outcome.result)
      else
        @account = outcome
        render(:new)
      end
    end

note:
    ActiveInteraction plays nicely with rail's `form_for` (and by extension, simple_form and Formtastic) as the outcome
    object returned from .new or .run quacks like an ActiveModel form object.
