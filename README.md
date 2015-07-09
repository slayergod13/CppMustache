# CppMustache
A Mustache &amp; Json Library for C++

#### Templates can be specified using mustache syntax: https://mustache.github.io/mustache.5.html
- Subset of mustache implemented (and some additions):
    - Literals
       - Support for SOME escape characters added (\r\n\t)
    - Variables
    - Partials
      - Added ability to isolate the child scope to prevent infinite recursion in partials (the context would no longer have access to its parent context)
      - {{>partial}} {{>>isolated-partial}}
    - Sections
       - Inverse
       - Conditional (for truthy values)
       - Iterator (for arrays)
       - And some new additions:
            - Comparisons:
                 - String Equality: {{#key=value}}
                 - String Inequality: {{#key!value}}
                 - Float Greater: {{#key>value}}
                 - Float Less: {{#key<value}}
                 - String In Set: {{#key$value1|value2|value3}}
                 - String Not In Set: {{#key^value1|value2|value3}}
