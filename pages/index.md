# CoffeeCup <☕/>
## Markup as CoffeeScript

This is a clone of @mauricemach [CoffeeCup](https://github.com/mauricemach/coffeekup).

I am renaming and trying to keep this project alive.

[Fork CoffeeCup on Github](https://github.com/gradus/coffeecup).

CoffeeCup is a templating engine for [node.js](http://nodejs.org) and browsers that lets you to write your HTML templates in 100% pure [CoffeeScript](http://coffeescript.org).

It was created in celebration of [whyday](http://whyday.org/), as an application of the concept used in [Markaby](https://github.com/markaby/markaby) ("Markup as Ruby", by Tim Fletcher and why the lucky stiff) to CoffeeScript.

Here's what a template written for CoffeeCup looks like:

    doctype 5
    html ->
      head ->
        meta charset: 'utf-8'
        title "#{@title or 'Untitled'} | A completely plausible website"
        meta(name: 'description', content: @description) if @description?
        
        link rel: 'stylesheet', href: '/css/app.css'
        
        style '''
          body {font-family: sans-serif}
          header, nav, section, footer {display: block}
        '''
        
        script src: '/js/jquery.js'
        
        coffeescript ->
          $(document).ready ->
            alert 'Alerts suck!'
      body ->
        header ->
          h1 @title or 'Untitled'
          
          nav ->
            ul ->
              (li -> a href: '/', -> 'Home') unless @path is '/'
              li -> a href: '/chunky', -> 'Bacon!'
              switch @user.role
                when 'owner', 'admin'
                  li -> a href: '/admin', -> 'Secret Stuff'
                when 'vip'
                  li -> a href: '/vip', -> 'Exclusive Stuff'
                else
                  li -> a href: '/commoners', -> 'Just Stuff'

        div '#myid.myclass.anotherclass', style: 'position: fixed', ->
          p 'Divitis kills! Inline styling too.'

        section ->
          # A helper function you built and included.
          breadcrumb separator: '>', clickable: yes
          
          h2 "Let's count to 10:"
          p i for i in [1..10]
          
          # Another hypothetical helper.
          form_to @post, ->
            textbox '#title', label: 'Title:'
            textbox '#author', label: 'Author:'
            submit 'Save'

        footer ->
          # CoffeeScript comments. Not visible in the output document.
          comment 'HTML comments.'
          p 'Bye!'

Interactive demo at [coffeekup.org](http://coffeekup.org).

