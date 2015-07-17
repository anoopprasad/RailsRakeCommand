adding gems into an application

gem 'devise'
gem 'foundation-rails'

commands you need to type

bundle 
rails g foundation:install
rails g devise:install
rails g devise user

rake db:create
rake db:migrate

rails g controller user index

add it in index action home controller 
before_action :authenticate_user!




      <nav class="top-bar">
        <ul class="title-area">
          <li class="name">
            <h1><%= link_to "Awesome Store", "" %></a></h1>
          </li>
        </ul>
        <section class="top-bar-section">
          <ul class="right">
            <li class="divider"></li>
            <li>
              <% if user_signed_in? %>
                <%= current_user.email %>
                
        <%= link_to "Sign out", destroy_user_session_path, :method => :delete %>
              <% else %>
                 <%= link_to "Sign in", new_user_session_path %>
              <% end %>
            </li>
          </ul>
        </section>
      </nav>
