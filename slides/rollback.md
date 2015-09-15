## Rollback

    class CreateOrder
      include Interactor

      def call
        order = Order.create(order_params)

        if order.persisted?
          context.order = order
        else
          context.fail!
        end
      end

      def rollback
        context.order.destroy
      end
    end

note:
    If any one of the organized interactors fails its context, the organizer stops, with any interactors that had
    already run are given the chance to undo themselves, in reverse order, via a defined rollback method.
