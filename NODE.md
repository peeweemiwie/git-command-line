#Command line for node.js

## npm WARN unmet dependency 

remove node_modules 

      $ rm -rf node_modules/
      
run 

      $ npm cache clean
      
then manually install failed packages 

      $ npm install lodash@3.7.0

## el captain ruby issues.

      sudo gem install -n /usr/local/bin compass (replace compass with whatever gem)

##Error: bind EADDRINUSE
Check to see if port is already taken.

    sudo lsof -i -P | grep 3000

if so:

    killnode all
    
## nunjucks

    json:
    {
        "component-name": {
        "color": "red"
        }
    }

    template method 1:
    {{ color }}

    template method 2:
    {% set templateName = componentSettings %}
    {{ templateName.color }}
