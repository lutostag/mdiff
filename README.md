# mdiff (motion diff)

A simple script to remove lines that have only been moved around in a diff. Useful for code reviews with lots of code movement/motion.

* ignores leading and trailing whitespace and is based on whole lines only
* holds the entire diff in memory, so be aware of that on very large diffs

Example usage:

    diff file1 file2 | ./mdiff
    git diff | ./mdiff

If you would only like 3 lines of context...

    git diff | ./mdiff | grep -EC 3 '^(\+|-)'

*Only dependency is any python.*
