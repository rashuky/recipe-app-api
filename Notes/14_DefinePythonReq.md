# Python requirements

How to set up required sw as a range, and why do you need this:
ex:

` Django>=3.2.4,<3.3`

X.Y.Z

- Z is a patch version (bug fixes that are backwards compatible, meaning if Z goes up code that uses the same minor version should continue to work!)
- Y is a minor version (larger bug fixes, new features still should be backward compatible)
- X is a major
- ,<3.3 means that the we don't want 