# MarioML Software Design Description
This document allows all contributors to be able to work in a consistent manner.
**NOTE** Everything is this document is subject to change.

## Image Naming Convention
Images are to be put under `images/character_name` *e.g. images/Mario/mario1.png*

## Github Naming Convention
(This is not too important, but it is best to adhere to some sort of convention)
- ### Branches:
    To create an effective branch name, follow the steps below:
    1. Type a `#` followed by the issue ID
    2. Add a short descriptor of the task
        - Perhaps you can use the issue title if it is concise
        - Make sure you use hyphens as separators
    An example of a good branch name should look like this: `#1-Add-More-Images`
- ### Issues:
    To raise a good issue, make sure you do the following:
    1. Make sure the title is clear and concise
    2. Give a description detailing exactly what the issue is
    3. Make sure you add labels - this allows other collaborators to filter through the issues and find yours more easily
    4. If you need help, assign someone to the task and they will be notified of your issue
- ### Version numbers:
    Once there are no bugs and it is at a state where everyone's work can be merged together, a new "version" will be released.
    This will happen when the code of everyone's has been reviewed and merged together, and the new version is fully stable and has no bugs.
    After a new version is created, a new branch is created to store the version so that collaborators can always backtrack if necessary.
    Previous branches that lead up to this version can be deleted, although it is not necessary.
    Make sure to update `CHANGELOG.md` and detail what has been added, fixed or changed.

## Style of Code
(if unsure, refer to [PEP 8](https://www.python.org/dev/peps/pep-0008/ "PEP 8 Style Guide"))

- ### Naming Convention:
    - Variables: `snake_case` *e.g. some_variable*
    - Subroutines: `snake_case` *e.g. some_function()*
    - Constants: `SCREAMING_SNAKE_CASE` *e.g SOME_CONSTANT*
- ### Indentation:
    - Spaces: 4
- ### Comments:
    - **Block Comments:** Single `#` and a `space` followed by the comment, on the line *before* the block of code.
    Keep it indented to the same level as the code, e.g.
    ```python
    import math

    # Calculate volume of a cylinder
    radius = input("Input radius of cylinder:")
    height = input("Input height of cylinder:")
    
    area_of_circle = 2 * math.pi * radius**2
    volume_of_cylinder = area_of_circle * height
    print(volume_of_cylinder)
    ```
    - **Inline Comments:** Single `#` and a `space` followed by the comment, on the same line as the line of code.
    **NOTE** Use sparingly and avoid stating the obvious, e.g.
    *Avoid* doing:
    ```python
    lower = input("Input lower value:")
    upper = input("Input upper value:")
    mid = (lower + upper) / 2
    mid = round(mid) # rounds the mid value
    ...
    ```
    Sometimes, this is useful:
    ```python
    lower = input("Input lower value:")
    upper = input("Input upper value:")
    mid = (lower + upper) / 2
    mid = round(mid) # allows the program to use mid as an index in later code
    ...
    ```
    - **Documentation Strings** `"""` before and after the documentation strings (aka docstrings).
    **NOTE** For multi-line docstrings, the `"""` that ends the docstring must be on a separate line after the docstring.
    For a one-line docstring, the closing `"""` is on the same line, e.g.
    ```python
    """ Multi-line docstring
    ...
    """

    """Single line docstring"""
    ```