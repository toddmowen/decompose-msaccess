Sorry, not yet ready for day-to-day use (but getting close)!

Current features:
* Decompose and compose MS-Access forms and queries to and from text.
* Decompose and compose tables, using one XML file for the table
  structure and one XML file for the data (if any).
* Decompose and compose database properties (e.g. start-up settings).
* Decompose and compose DLL references.

Planned features:
* Decompose and compose table relations.
* Decompose other MS-Access objects such as reports, modules
  (should be very easy, similar to forms and queries).

Limitations and known issues:
* No support for code-signing or encryption.
* Composing tables that contain medium to large OLE objects
  (e.g. hundreds of kilobytes) is very slow.
