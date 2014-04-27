### csv-pivot

As per [this blog post](http://bobjflong.co/site/posts/csv-1397599801.html), I use this script to summarize csv content.

```shell
# group by 1st column, then group by 0th column, then avg by 2nd column

csvpivot '(Call gb 1)' '(Call gb 0)' '(Call ab 2)'
```

To run it, you need drog_lisp. I'd recommend cloning that repo. Once you have it, you need an executable to execute standalone scripts like this one. Eg:

```ruby
#!/usr/bin/env ruby

require 'drog_lisp'

LispMachine.run File.read(ARGV[0]), { FILE: ARGV[0], DIR: File.expand_path(File.dirname(ARGV[0])) }
```
