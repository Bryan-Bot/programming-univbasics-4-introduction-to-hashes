# Ruby Hashes

## Learning Goals

- Define a Ruby `Hash`
- Define `Hash` keys and values
- Create a `Hash` using its implicit form
- Create a `Hash` with `Hash.new`

## Introduction

Up until this point, we've stored our data in list-form using `Array`s. An `Array`
is like a numbered list. It stores a group of items which are accessible via
their location, or index number, in the list.  

`Hash`es allow us to store named, or associated, data like a dictionary or an
address book. `Hash`es allows us to store more complex collections of
information than the `Array`s we've seen so far.

## Define a Ruby Hash

A _`Hash`_ is a collection of data that is separated into pairs of keys and values.
Each key/value pair makes up one unit in the `Hash`. The entire collection of
key/value pairs, which are comma separated, is enclosed in curly braces `{}`:

```ruby
{"key" => "value", "another_key" => "another value"}
```

## Define Hash Keys and Values

In earlier lessons, we discussed variable assignment:

```ruby
apple = "a delicious fruit"
garlic = "an herb used for flavoring in many cuisines"
cheese = "a dairy product derived from the coagulation of milk protein"
```

Variables are great for storing single bits of data so that we can _look up_
the data later.

Key/value pairs are similar, but they use "two-names" to identify the place
where the variable content goes. Think about latitude and longitude. By knowing
a latitude (38&deg; North) and a longitude (0&deg; West), we can find an exact
point on Earth.  The `Hash` name and the key within it is a "coordinate" for a
value. You use those coordinates to retrieve a value and to store a value.

Image

Using a `Hash`, we could represent the same values from above like so:

```ruby
foods = {
  "apple" => "a delicious fruit",
  "garlic" => "an herb used for flavoring in many cuisines",
  "cheese" => "a dairy product derived from the coagulation of milk protein"
}
```

The above `Hash` (`foods`) has three key/value pairs. As such there are
**three** possible coordinates: `foods["apple"]`,  `foods["garlic"]`, and
`foods["cheese"]`.

The relationship between a key and value is indicated by using the `=>` symbol
(sometimes lovingly referred to as a "hash-rocket" because it looks like a
little sideways rocket inside of a `Hash`).

Hash keys can be any type of data but most of the time we use [strings][] (as
seen in the above example) or [symbols][]:

```ruby
{:name => "John Henry", :occupation => "Steel-driving man"}
```

Hash values can also be any type of data, including `Array`s and even other
`Hash`es (remember "nesting?")!

```ruby
{:item => "banana", :price => 0.89, :quantity => 6, :description => "a delicious fruit"}
```

## Create a Hash

The easiest way to create a `Hash` is to write it out as we've seen in the
examples so far.

```ruby
new_hash = {
  :created => Time.now,
  :message => "Hello world!"
}
#=> {:created=>2019-04-10 14:05:33 -0400, :message=>"Hello world!"}
```

Once created, we can access this `Hash` with our `new_hash` variable:

```ruby
new_hash
#=> {:created=>2019-04-10 13:42:27 -0400, :message=>"Hello world!"}
```

Note that because we didn't provide a second coordinate (a key) but instead
just provided the hash name, IRB printed out the whole `Hash`. With a big
`Hash`, this would fill up our screen and scroll for pages and pages. But for a
small `Hash`, it's not bad.

Alternatively, we can use `Hash.new` to create a new `Hash`:

```ruby
second_new_hash = Hash.new
#=> {}
```

This is the same as writing:

```ruby
second_new_hash = {}
#=> {}
```

## Conclusion

We're just getting started with `Hash`es, but hopefully you can already see why
they might be useful. With `Hash`es, we can use `Hash` keys as a way of
_naming_ individual pieces of data. Including multiple key/value pairs allows us
to _associate_ different bits of data, bundling them all up into one object.

Now that we can create `Hash`es and store data as key/value pairs, in the next
lesson, we'll look at how we can access that data. Given a dictionary and a
particular word, we can look up the definition of that word. Similarly, given
a `Hash` and a key in that `Hash`, we can look up the value assigned to that key.

## Resources

- [Intro to Hashes Video][video]
- [Ruby Hash Class][hashes]

[video]: https://www.youtube.com/embed/0JSsFQGYaeA
[hashes]: https://ruby-doc.org/core-2.5.0/Hash.html
[symbols]: https://ruby-doc.org/core-2.5.0/Symbol.html
[strings]: https://ruby-doc.org/core-2.5.0/String.html
[integers]: https://ruby-doc.org/core-2.5.0/Integer.html
[histograms]: https://en.wikipedia.org/wiki/Histogram#Examples
[melville]: https://en.wikipedia.org/wiki/Herman_Melville
