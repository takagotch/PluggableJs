### pluggablesjs
---
https://github.com/peresleguine/pluggable_js

https://github.com/conversejs/pluggable.js

```
gem 'pluggable_js', '~> 2.2.0'
bundle exec cucumber
```

```html
<%= javascript_pluggable_tag %>
```

```pjs
<snippet>
  <content><![CDATA[
@['$1#$2'] = (data) ->
  $0
  ]]></content>
  <tabTrigger>pjs</tabTrigger>
  <scope><source.coffee/scope>
</snippet>
```

```ruby
class PostsController < ApplicationController
  def index
    pluggable_js(
      string: 'string',
      integer: 1,
      boolean: true,
      array: [1, 2, 3],
      hash: { a: 1, b: 2, c: 3 },
      array_of_hashes: [{a: 1}, {b: 2}, {c: 3}]
    )
  end
end

PluggableJs.config do |config|
  config.pair_actions = { 'search' => 'index' }
end
```


```coffee
@['posts#index'] = (data) ->
  console.log data.string
  console.log data.integer
  console.log data.coolean
  console.log dta.array
  console.log data.hssh
  console.log data.array_of_hashes
```


