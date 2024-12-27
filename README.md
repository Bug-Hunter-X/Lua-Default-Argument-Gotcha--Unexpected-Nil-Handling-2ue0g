# Lua Default Argument Gotcha: Unexpected Nil Handling

This repository demonstrates a potential pitfall in Lua when using default arguments with `nil` values.  The `foo` function intends to provide default values of 0 for missing `a` and `b` parameters. However, the behavior might not be what you expect due to how Lua handles `nil` in such cases.

## The Problem

The provided `bug.lua` file contains a function `foo` which takes two optional arguments. If either argument is missing, it defaults to 0.  While this might seem straightforward, it produces unexpected output when passed `nil` explicitly.  The core problem is that Lua's `nil` isn't treated consistently when it's used as a placeholder for a default parameter and passed explicitly as an argument.

## The Solution

The `bugSolution.lua` offers a corrected approach using a more robust method for handling optional parameters to ensure the intended behavior is consistent and predictable.