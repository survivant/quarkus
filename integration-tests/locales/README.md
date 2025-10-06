Locales (i18n)
==============

Native-image built applications do not have all [locales](https://docs.oracle.com/javase/tutorial/i18n/locale/index.html) included by default, as this
unnecessarily inflates the executable size.

One can configure native-image to [include locales](https://www.graalvm.org/latest/reference-manual/native-image/dynamic-features/Resources/#locales). This is mirrored in Quarkus configuration.

All
---
The "All" test uses a special string "all" that internally translates as Locale.ROOT and is
interpreted as "Include all locales".

Some
----
The "Some" test uses a list of picked locales and verifies that only those are available.
