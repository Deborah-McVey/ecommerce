"Fullstack E-Commerce: Ruby on Rails 7, Hotwire, Tailwind CSS, Stripe, PostgreSQL" by Conner Jensen

https://www.youtube.com/watch?v=hURUMwdCWuI&t=5516s

rails new ecommerce --css tailwind

Stripe - checkout

Devise - authentication

PostgreSQL - database

Render - deployment

https://github.com/connerj70/ecomm

Gemfile
gem 'Devise'
bundle i
rails g devise:install

Depending on your application's configuration some manual setup may be required:

  1. Ensure you have defined default url options in your environments files. Here
     is an example of default_url_options appropriate for a development environment
     in config/environments/development.rb:

       config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }

     In production, :host should be set to the actual host of your application.

     * Required for all applications. *

  2. Ensure you have defined root_url to *something* in your config/routes.rb.
     For example:

       root to: "home#index"
     
     * Not required for API-only Applications *

  3. Ensure you have flash messages in app/views/layouts/application.html.erb.
     For example:

       <p class="notice"><%= notice %></p>
       <p class="alert"><%= alert %></p>

     * Not required for API-only Applications *

  4. You can copy Devise views (for customization) to your app by running:

       rails g devise:views
       
     * Not required *

application.css.scss
application.tailwind.css
@import 'font-awesome'
home_controller.rb
index.html.erb     