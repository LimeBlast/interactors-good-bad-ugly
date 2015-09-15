##  Organizers

    class PlaceOrder
      include Interactor::Organizer

      organize CreateOrder, ChargeCard, SendThankYou
    end

note:
    And thanks to organisers, and the shared context which gets passed between them in the order defined, you're able to
    specify entire chains of events.
