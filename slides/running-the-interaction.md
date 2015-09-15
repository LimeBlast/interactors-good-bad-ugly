##  Running the interaction

    # GET /accounts/:id
    def show
      @account = find_account!
    end

    private

    def find_account!
      outcome = FindAccount.run(params)

      if outcome.valid?
        outcome.result
      else
        fail ActiveRecord::RecordNotFound, outcome.errors.full_messages.to_sentence
      end
    end

note:
    Once you've built your interactors you're able to run them in one of two ways: .run and .run!. Both have you pass in
    your defined parameters as a hash, with the only different between the two being the outcome. .run returns an outcome
    object which you're able to test for success, and react accordingly...
