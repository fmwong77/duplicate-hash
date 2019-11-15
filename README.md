# duplicate-hash
Create a method that takes in an array of integers with duplicates and outputs a hash of how often each number occurs.

input: [1,2,2,3,3,4,5,5,5]
output: {1:1, 2:2, 3:2, 4:1, 5:3}

This is an excellent way to prepare data for statistics or graphing.

Answer:

arr = [1,2,2,3,3,4,5,5,5]

# arr.inject(Hash.new(0)) {|h,i| h[i] += 1; h }

hash = {}
arr.each do |ele|
  hash[ele] ||= 0
  hash[ele] += 1
end

hash
