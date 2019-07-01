## Ruby and Rails Snippets for Visual Studio Code 

Very similar to [Vense's rails extension](https://marketplace.visualstudio.com/items?itemName=Vense.rails-snippets) but with my own twists and added snippets :smile:

I plan to modify and extend this snippets pack as time goes on

##### Supported file extensions

- Ruby (.rb)
- EmbeddedRuby (html.erb)
- Slim (html.slim)

##### tips
1. `control/command + space` loads the snippet suggestions if they aren't shown right away.
2. `$1` is where the snippet starts. `$0` is where the snippet ends.
3. Press `tab` to move onto the next part of a snippet.
___
## - `html.erb` / Rails -
#### [pre] template exec tag `<% %>`
#### [pe] template render tag `<%= %>`
#### [preb] template exec tag block `<%`
```javascript
<% $1 %>
  $0
<% end %>
```
#### [peb] template render tag block `<%=`
```javascript
<%= $1 %>
  $0
<% end %>
```
#### [each] forEach loop
```javascript
<% ${1:items}.each do |${2:item}| %>
  $0
<% end %>
```
#### [form_for] form_for
```javascript
<%= form_for ${1:variable} do |${2:f}| %>
  $0
<% end %>
```
#### [timezone] select time zone 
```javascript
<%= f.time_zone_select :${1:id_name} %>
```
#### [rangefield] range_field
```javascript
<%= range_field (:${1:model_name}, :${2:id_name}, in: ${3:1..100}) %>
```
#### [selecttag] select_tag
```javascript
<%= select_tag (:${1:id_name}, :${2:options_for_select(options)} %>
```
#### [colorfield] color_field
```javascript
<%= color_field :${$1:id_name} %>
```
#### [options_for_select] options_for_select
```ruby
options_for_select([${1:options}])$0 
```
#### [render] render
```javascript
<%= render ${1:path} %>$0 
```
#### [rendervar] render variable
```javascript
<%= render ${1:path}, ${2:var1}: ${3:var2} %>
```
#### [lt] link_to
```javascript
<%= link_to '${1:text}', ${2:path} %>
```
#### [ltc] link_to_class
```javascript
<%= link_to '${1:text}', ${2:path}, class:'${3:class}' %>
```
#### [ltmd] link_to_method_data
```javascript
<%= link_to '${1:link_text}', ${2:path}, method: '${3:method}', data:{ ${4:data} } %>
```
#### [ltmdc] link_to_method_data_class
```javascript
<%= link_to '${1:link_text}', ${2:path}, method: '${3:method}', data:{ ${4:data} }, class:'${5:class}' %>
```
#### [ltmcon] link_to_method_confirm
```javascript
<%= link_to \"${1:link_text}\", ${2:path}, method: \"${3:method}\", data:{ confirm: \"${4:confirm}\"} %>
```
#### [ltmconc] link_to_method_confirm_class
```javascript
<%= link_to \"${1:link_text}\", ${2:path}, method: \"${3:method}\", data:{ confirm: \"${4:confirm}\"}, class:\"${5:class}\" %>
```
#### [submit] submit
```javascript
<%= f.submit %>$0
```
#### [label] label
```javascript
<%= f.label :${1:id_name}, '${2:text}' %>$0
```
#### [numberfield] number_field
```javascript
<%= f.number_field (:${1:id_name}, in: ${2:1.0..20.0}, step: ${3:0.5}) %>$0
```
#### [timefield] time_field
```javascript
<%= f.time_field :${1:id_name} %>
```
#### [hiddenfield] hidden_field
```javascript
<%= f.hidden_field :${1:id_name} %>
```
#### [emailfield] email_field
```javascript
<%= f.hidden_field :${1:id_name} %>
```
#### [urlfield] url_field
```javascript
<%= f.url_field :${id_name} %>
```
#### [passwordfield] password_field
```javascript
<%= f.password_field :${id_name} %>
```
#### [textarea] text_area
```javascript
<%= f.text_area :${id_name} %>
```
#### [checkbox] check_box
```javascript
<%= f.check_box :${id_name} %>
```
#### [textfield] text_field
```javascript
<%= f.text_field :${id_name} %>
```
#### [datefield] date_field
```javascript
<%= f.date_field :${id_name} %>
```
#### [datetime_field] datetime_field
```javascript
<%= f.datetime_field :${1:id_name} %>
```
#### [radiobutton] radio_button
```javascript
<%= f.radio_button :${1:name}, :value => '${2:value}' %>
```
#### [input] input
```javascript
<%= f.input :${1:id}, label: '${2:text}' %>
```
#### [path] path
```ruby
${1:path}_path
```
#### [newpath] new_path
```ruby
new_${1:path}_path
```
#### [editpath] edit_path
```ruby
edit_${1:path}_path(${2:variable})
```
#### [if] if statement 
```javascript
<% if $1 %>
  $2
<% end %>
```
#### [else] else
```javascript
<% else %>
```
#### [elsif] elsif
```javascript
<% elsif ${1:truevalue} %>
```
#### [if else] if else statement 
```javascript
<% if $1 %>
  $2
<% else %>
  $3
<% end %>
```
#### [if elsif]
```javascript
<% if $1 %>
  $2
<% elseif %>
  $3
<% end %>
```
#### [if elsif else]
```javascript
<% if $1 %>
  $2
<% elseif %>
  $3
<% else %>
  $4
<% end %>
```
#### [unless] unless
```javascript
<% unless ${1:falsevalue} %>
  $2
<% end %>
```
#### [unless else] unless
```javascript
<% unless ${1:falsevalue} %>
  $2
<% else %>
  $3
<% end %>
```
#### [%end] end
```javascript
<% end %>
```
___

# `.rb` / Rails
#### [only] 
```ruby
only: %i[${1:method}]
```
#### [except] 
```ruby
except: %i[${1:method}]
```
## Rails Routing
#### [get] get route 
```ruby
get '/${1:route}', to: '${2:controller}#${3:method}'
```
#### [post] post route
```ruby
post '/${1:route}', to: '${2:controller}#${3:method}'
```
#### [patch] patch route
```ruby
patch '/${1:route}', to: '${2:controller}#${3:method}'
```
#### [put] put route
```ruby
put '/${1:route}', to: '${2:controller}#${3:method}'
```
#### [delete] delete route
```ruby
delete '/${1:route}', to: '${2:controller}#${3:method}'
```
#### [res] resources
```ruby
resources :${res_name}
```
#### [resb] res_block
```ruby
resources :${1:res_name} do
  $2
end
```
#### [rescb] res_collection_block
```ruby
resources :${1:res_name} do
  collection do
    $2
  end
end
```
#### [resmem] res_member
```ruby
resources :${1:res_name} do
  member do
    $2
  end
end
```
#### [re] resources
```ruby
resource :${res_name}
```
#### [reb] res_block
```ruby
resource :${1:res_name} do
  $2
end
```
#### [recb] res_collection_block
```ruby
resource :${1:res_name} do
  collection do
    $2
  end
end
```
#### [remem] res_member
```ruby
resource :${1:res_name} do
  member do
    $2
  end
end
```
#### [mem] member block
```ruby
member do
  $1
end
```
#### [collection] collection block
```ruby
collection do
  $1
end
```
## Redirect
#### [render] render path
```ruby
render ${1:path}
```
#### [redirect_to] redirect_to
```ruby
redirect_to ${1:path}
```
#### [redirect_to_msg] redirect_to with msg
```ruby
redirect_to ${path}, notice: '${msg}'
```
## Model
#### [has_one] has_one 
```ruby
has_one :$0
```
#### [dep] dependant
```ruby
dependent: :${1:id}
```
#### [has_one_dep] has_one_dependent
```ruby
has_one :${1:id}, dependent: :${2:type}
```
#### [has_many] has_many
```ruby
has_many :$0
```
#### [has_many_through] has_many_through
```ruby
has_many :${1:model1}, through: :${2:model2}
```
#### [has_many_dependent] has_many_dependent
```ruby
has_many :${1:id}, dependent: :${2:type}
```
#### [belongs_to] belongs_to
```ruby
belongs_to :
```
#### [belongs_to_cache] belongs_to_cache
```ruby
belongs_to :${1:id}, cache: ${2:true}
```
#### [has_and_belongs_to_many] belongs_to_cache
```ruby
has_and_belongs_to_many :${1:id}
```
## Columns
#### [add_column] add_column
```ruby
add_column :${1:table}, :${2:column}, :${3:type}
```
#### [add_reference] add_reference
```ruby
add_reference :${1:table}, :${2:column}, foreign_key: tru
```
#### t.[x] table column property
x = binary/boolean/date/datetime/decimal/float/integer/references/string/
text/time/timestamp/timestamps
## Params
#### [params] params
```ruby
params.require(:${1:id_name}).permit(:${2:variable})
```
#### [req] req
```ruby
require(:$1)$0
```
#### [permit] permit
```ruby
permit(${1:id});
```
## Controller
#### [controller] controller
```ruby
class ${1:Name}Controller < ApplicationController
  $2
end
```
#### [index] index method
```ruby
def index 
  $1
end 
```
#### [create] create method
```ruby
def create 
  $1
end 
```
#### [new] new method
```ruby
def new 
  $1
end 
```
#### [edit] edit method
```ruby
def edit 
  $1
end 
```
#### [show] show method
```ruby
def show 
  $1
end 
```
#### [update] update method
```ruby
def update 
  $1
end 
```
#### [destroy] destroy method
```ruby
def destroy 
  $1
end 
```
#### [crud] full crud
```ruby
def index
end
def new  
end
def create
end
def edit
end
def update
end
def show
end
def destroy
end
```
#### [before_action] before_action
```ruby
before_action :id|
```
#Ruby
|Prefix||
|---|---|
|if|if $1<br>&nbsp;&nbsp;$2<br>end|
|if else|if $1<br>&nbsp;&nbsp;$2<br>else<br>&nbsp;&nbsp;$3<br>end|
|if elsif|if $1<br>&nbsp;&nbsp;$2<br>elsif $3<br>&nbsp;&nbsp;$4<br>end|
|if elsif else|if $1<br>&nbsp;&nbsp;$2<br>elsif $3<br>&nbsp;&nbsp;$4<br>else<br>&nbsp;&nbsp;$5<br>end|
|first|first(quantity)|
|find_by|find_by(id: params[:id])|
|where|where(condition)|
|increment|increment(:id)|
|order|order(id: :desc)|
|limit|limit(quantity)|
|def|def {name}<br><br>end|