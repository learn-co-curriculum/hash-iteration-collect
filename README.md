# Hash Iteration with `#collect`

## Overview

We'll use `#collect` to iterate over a hash. 

## Objectives

1. Identify when `#collect` is most often used when iterating over hashes.
2. Give examples of using `#collect` to iterate over a hash.

## Using `#collect`

*Note: `#collect` is actually an alias for `#map`. That means the two methods can be used interchangeably, and effect the same behavior*.

We use `#collect` to iterate over a collection of data, such as an array or a hash, and return a collection of the data therein. 

We have seen it used with arrays to iterate over an array, operate on the data it contains, and return a collection with this altered data. 

When working with hashes, we'll most often see `#collect` used to collect the values of the hash's keys and/or collect data that we've operated on over the course of an iteration. 

Let's take a look at an example.

### `#collect`ing Hash Values

Let's use `#collect` to return all of the values of the keys in a given hash.

In this example, we are once again the managers at Chuck E. Cheese's. Chuck E. Cheese's is still a great place to have a birthday party, and, shockingly, the same three birthdays are still going on.

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
birthday_kids = {
	"Timmy" => 9, 
	"Sarah" => 6, 
	"Amanda" => 27
}

birthday_kids.collect do |kids_name, age|
	age
end

# => [9, 6, 27]
```

Note that the return value is an *array* of the values we collected. 

## Advanced Example

You might have noticed that our previous example didn't operate on the data we were collecting. Let's step it up a level. In this example, we'll iterate over the `birthday_kids` hash using `#collect` and return the age of each child, in dog years:

```ruby
birthday_kids.collect do |name, age|
	age * 7
end
```

In this case, we are multiplying the value of each `age` by `7` and collecting the return values of that multiplication into a new array. The above method call would return:

```ruby
[63, 42, 189]
```


