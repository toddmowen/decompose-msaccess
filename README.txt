----------------------------------------------------------------------------
THIS PROJECT HAS BEEN ABANDONED

I used this tool for a couple of jobs, but ultimately found the experience
disappointing, because it didn't really fit my workflow. I was using
Mercurial for source control, and hoped to be able to review and commit
changes to an Access application as easily as I could if I was working on
textual source files. Unfortunately:

1. It is too slow. In particular, the "database-at-once" approach to
   decomposing and recomposing does not scale well to large applications.

2. There is too much "noise" in diffs. Just about any design change in
   Access tends to result in a slew of tiny updates to various seemingly
   unimportant properties, including some opaque binary properties whose
   values are exported as hex strings. The developer either has to commit
   only those that seem relevant (at the risk of corrupting the MDB) or
   blindly commit everything (obscuring the actual purpose of the commit).

3. Less critical, but inconvenient, is that it's hard to select and commit
   just a subset of the currently changed objects. It's even harder to
   *revert* just a subset of changes.

Hopefully better solutions can be found, but it's hard to imagine that
source control for Access projects will ever be as easy and natural as it
is for a hierarchy of plain old source files.

For further discussion and alternatives see this thread:
http://stackoverflow.com/questions/187506
----------------------------------------------------------------------------


Current features:
* Decompose MS-Access forms, queries, reports, modules, macros
  and data access pages to text files.
* Decompose table structure and relationships to SQL files.
* Decompose table data to XML files.
* Decompose database properties (e.g. start-up settings).
* Decompose DLL references.

Limitations and known issues:
* No support for object permissions.
* No support for ADP projects (currently only tested with MDB files).
* No support for code-signing or encryption.
