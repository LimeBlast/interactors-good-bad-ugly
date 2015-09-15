##  Errors

    class FindAccount < ActiveInteraction::Base
      integer :id

      def execute
        account = Account.not_deleted.find_by_id(id)

        if account
          account
        else
          errors.add(:id, 'does not exist')
        end
      end
    end

note:
    If your logic is able to perform successfully, you simply return the result of the operation, but if something goes
    wrong, you return an error object with a description of the problem.
