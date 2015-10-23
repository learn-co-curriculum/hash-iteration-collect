# Hash Iteration with `#collect`

## Objectives

1. Learn how to use `#collect` to iterate over a hash. 

## Using `#collect`

We use `#collect` to iterate over a collection of data, such as an array or a hash, and return a collection of the data therein. 

We have seen it used with arrays to iterate over an array, operate on the data contained there and return a collection of this altered data. 

When working with hashes, we'll most often see `#collect` used to collect the values of the hash's keys and/or collect data that we've operated on over the course of an iteration. 

Let's take a look at an example.

### `#collect`ing Hash Values

Let's use `#collect` to return all of the values of the keys in a given hash.

In this example, we are the managers at Chucky Cheese. Chucky Cheese is a great place to have a birthday party, and there are several birthdays going on here today. 

We will be operating on the following hash that tracks birthday kids and their associated ages:

```ruby
birthday_kids = {
	"Timmy" => 9, 
	"Sarah" => 6, 
	"Amanda" => 27
}
```

Our managers have asked us to give them the list of ages of the birthday kids so they know how many candles to buy for the birthday cakes. Let's iterate over the `birthday_kids` hash and collect the ages.

```ruby
birthday_kids.collect do |kids_name, age|
	age
end

=> [9, 6, 27]
```

Note that the return value is an *array* of the values we collected. 