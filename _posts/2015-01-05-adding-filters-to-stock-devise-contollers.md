---
layout: post
title: "Adding Filters to Stock Devise Controllers"
tags: [rails, development, tips]
---
First, we’ll create a module in config/initializers/devise_filters.rb where we’ll implement a method to add all the filters to Devise that we want. We also need to make sure this module calls this method upon initialization so that our filters get added upon startup (important for the production environment).

## Put this somewhere it will get auto-loaded, like config/initializers
{% highlight ruby %}
module DeviseFilters
  def self.add_filters
    # Example of adding a before_filter to all the Devise controller
    # actions we care about.
    [
      Devise::SessionsController,
      Devise::RegistrationsController,
      Devise::PasswordsController
    ].each do |controller|
      controller.before_filter :prepare_for_mobile
    end

    # Example of adding one selective before_filter.
    Devise::RegistrationsController.before_filter :check_invite_code, :only => :new
  end

  self.add_filters
end
{% endhighlight %}

At this point, we’re in the same place we left off back in August: we can add filters to Devise controller actions, but in development mode the second request reloads all the Devise classes and all our filters are gone.To address this, we need to add a bit of code to the end of the initializer block in config/environments/development.rb like so:

{% highlight ruby %}
MyApp::Application.configure do
  # ...the usual stuff ...

  # Stuff to do on each request
  config.to_prepare do
    DeviseFilters.add_filters
  end
end
{% endhighlight %}

This tells Rails to call your DeviseFilters.add_filters method before each new request in development mode, after the classes have been reloaded.

With respect to Scott W.Bradley. Link to the [source](http://scottwb.com/blog/2012/02/16/revisited-adding-filters-to-stock-devise-controllers/){:target="_blank"}.

{% include JB/setup %}