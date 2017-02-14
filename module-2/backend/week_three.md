## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
rails new
2. What do Models generally inherit from in rails?
ApplicationRecord
3. What do Controllers generally inherit from in a rails project?
ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
Within the routes file, include "resources :horse, only: :show"
5. What rake task is useful when looking at routes, and what information does it give you?
rake routes is AMAZING. It gives you the prefix that you would use when referencing a path, the HTTP verb, the URI pattern and the Controller#Action (controller method). 
6. What is an example of a route helper? When would you use them?
hmmm horses_path or horse_path(horse) ? You would use them in lieu of using an href path. 
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
Path is going to start from the root '/' of your directory, when url is going to include an http:// address? 
8. What are strong params and why are the necessary?
It is kind of like an additional layer of validating a new object that the user is entering. They are necessary when the user is entering information because we can't trust the user. 
9. What role does `form_for` play in helping us create our forms?
It creates an object(s) oriented form! 
10. How does `form_for` know where to submit the user's input?
The controller passing through instance variables to the view, which are rendered in the form. In creating a form using form_for you pass through the model object or objects that the form needs to know about. EG if the user is to create a new object, the controller's new method is going to pass through a new object to the view, and the form will recognize it as the object. 
11. Create a form using a `form_for` helper to create a new `Horse`. 
class HorseController < ApplicationController
  def new
    @horse = Horse.new
  end 
  
  def create 
    @horse = Horse.new(horse_params)
    if @horse.save 
      redirect_to @horse
    else
      render :new
     end
   end 
   
  private 
    def horse_params
      params.require(:horse).permit(:name, :breed)
    end 
  end 
   

<%= form_for(@horse) do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>
  
  <%= f.label :breed %>
  <%= f.text_field :breed %>
  
  <%= f.submit %>
<% end %>
  
   

12. Why do we want to validate our models?
If we didn't specify which values are required to complete a model object, it would be easy to create empty objects in the database which isn't ideal.
