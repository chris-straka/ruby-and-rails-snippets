## Ruby and Rails Snippets for Visual Studio Code 

Pretty much [Vense's ruby extension](https://marketplace.visualstudio.com/items?itemName=Vense.rails-snippets) with my own twists.

I intend to add more over time. 

##### Supported languages (file extensions)

- Ruby (.rb)
- EmbeddedRuby (html.erb)
- Slim (html.erb)

##### tips
1. `control/command + space` loads the snippet suggestions if they aren't shown right away.
2. `$1` is where the snippet starts. `$0` is where the snippet ends.
3. Press `tab` to move onto the next part of a snippet.
4. You can usually hit `tab` long before you finish typing a snippet

## - ERB / Rails -
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
# Ruby

|Prefix||
|---|---|
|only|only: [:id]|
|except|except: [:id]|
## Route
|Prefix||
|---|---|
|get|`get "/$1", to: "$2"`|
|post|`post "/$1", to: "$2"`|
|patch|`patch "/$1", to: "$2"`|
|put|`put "/$1", to: "$2"`|
|delete|`delete "/$1", to: "$2"`|
|res|`resources :res_name`|
|res_block|resources :res_name do<br>  <br>end|
|res_collection_block|resources :res_name do<br>&nbsp;&nbsp;collection do<br>&nbsp;&nbsp;&nbsp;&nbsp;<br>&nbsp;&nbsp;end<br>end|
|res_member_block|resources :res_name do<br>&nbsp;&nbsp;member do<br><br>&nbsp;&nbsp;end<br>end|
|re|resource :res_name|
|re_block|resource :res_name do<br>  <br>end|
|re_collection_block|resource :res_name do<br>&nbsp;&nbsp;collection do<br>&nbsp;&nbsp;&nbsp;&nbsp;<br>&nbsp;&nbsp;end<br>end|
|re_member_block|resource :res_name do<br>&nbsp;&nbsp;member do<br><br>&nbsp;&nbsp;end<br>end|
|member_block|member do<br><br>end<br>|
|collection_block|collection do<br><br>end|


## Redirect
|Prefix||
|---|---|
|render|render path|
|redirect_to|redirect_to path|
|redirect_to_msg|redirect_to path, notice: "msg"|

## Model
|Prefix|shortcut||
|---|---|---|
|***relationship***|||
|has_one||has_one :|
|dependent||dependent: :id|
|has_one_dependent||has_one :id, dependent: :type|
|has_many||has_many :|
|has_many_through||has_many :model1, through: :model2|
|has_many_dependent||has_many :id, dependent: :type|
|belongs_to||belongs_to :|
|belongs_to_cache||belongs_to :id, cache: true|
|has_and_belongs_to_many|habtm|has_and_belongs_to_many :id|
|***column***|||
|t.binary|tcbi|t.binary :|
|t.boolean|tcb|t.boolean :|
|t.date|tcda|t.date :|
|t.datetime|tcdt|t.datetime :|
|t.decimal|tcd|t.decimal :|
|t.float|tcf|t.float :|
|t.integer|tci|t.integer :|
|t.references|tcr|t.references :|
|t.string|tcs|t.string :|
|t.text|tct|t.text :|
|t.time|tcti|t.time :|
|t.timestamp|tcts|t.timestamp :|
|t.timestamps|tctss|t.timestamps|
|validates||validates :column, presence: true|
|add_column||add_column :table, :column, :type|
|add_reference||add_reference :table, :column, foreign_key: true|
|**Feature**|||

## Params
|Prefix||
|---|---|
|params|params.require(:id_name).permit(:variable)|
|require|require(:id_name)|
|permit|permit(:id_name)|

## Controller
|Prefix|shortcut||
|---|---|---|
|controller||class Controller < ApplicationController<br> <br>end|
|index||def index<br><br>end|
|create||def create<br><br>end|
|new||def new<br><br>end|
|edit||def edit<br><br>end|
|show||def show<br><br>end|
|update||def update<br><br>end|
|destroy||def destroy<br><br>end|
|CRUD||def index<br><br>end<br><br>def new<br><br>end<br><br>def create<br><br>end<br><br>def edit<br><br>end<br><br>def update<br><br>end<br><br>def show<br><br>end<br><br>def destroy<br><br>end|
|before_action|ba|before_action :id|
## Others
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