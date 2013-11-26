# Composite Primary Keys in CakePHP 2.x

## Note

This is not a good pratice for database modeling, so, the recommended is use just a simple primary key:

```
    -- in mysql
    id int not null primary key

    -- in postgresql
    id serial primary key
```

## Instructions

- Download (not clone) this repostory with zip (link at right).
- Extract the zip file in a temp folder (out of your CakePHP project)
- Open the folder created and copy the folder Lib. This folder contain all files you need.
- Paste in your app folder for your Project, like that: /your-project/app/<paste here>
- Now you need add some code in your mode with composite primary keys:

```
    public $primaryKey = false;
    public $compositePrimaryKey = array('key_one', 'key_two', 'key..........');
```

**Done!**

## Model id

Now, if you do `$this->YOUR_MODEL->id`, you get an array like that:

```
    'id' => array(
        'key_one' => value_of_key,
        'key_two' => value_of_key,
        'key_three' => value_of_key
    )
```

## You wanna help? Send a pull request!

*Sorry for my english, and of course, THANKS SO MUCH!*


