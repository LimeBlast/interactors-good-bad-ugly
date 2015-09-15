##  form_for

    <%= form_for @account, as: :account, url: accounts_path do |f| %>
      <%= f.text_field :first_name %>
      <%= f.text_field :last_name %>
      <%= f.submit 'Create' %>
    <% end %>

note:
    Allowing for the form markup you're already used to.
