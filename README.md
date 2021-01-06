# ror-todo

勉強のためruby on railsを使ってTO-DOを作る  

### rubyとは？

「まつもと ゆきひろ」が作った単語  
１９９３年２月２４日生まれた単語  

### 基本勉強

https://www.tutorialspoint.com/ruby/index.htm

### install ruby for windows 10

https://rubyinstaller.org/downloads/


### check ruby version

```
ruby --version
ruby 3.0.0p0 (2020-12-25 revision 95aff21468) [x64-mingw32]

gem --version
3.2.3
```

### install rails

```
gem install rails
```

### check rails version
```
rails --version
Rails 6.1.0
```

### rbenv

https://github.com/rbenv/rbenv  

rbenv support MacOS, Linux  
not support windows 10  

### create project

```
rails new todo
```

### run server

optionを見る
```
rails s --help
```

サーバーを実行する
```
rails s
```

### rails MVC

https://guides.rubyonrails.org/getting_started.html  


##### config/routes.rb
```ruby
Rails.application.routes.draw do
  get "/", to: "todo#index"
end
```

```
rails generate controller Todo index --skip-routes
```

##### app/views/todo/index.html.erb
```html
<h1>hello</h1>
```

### rails MVC key value

##### app/controllers/todo_controller.rb
```ruby
class TodoController < ApplicationController
  def index
    @key = 'value'
  end
end
```

##### app/views/todo/index.html.erb
```html
<h5><%= @key %></h5>
```
