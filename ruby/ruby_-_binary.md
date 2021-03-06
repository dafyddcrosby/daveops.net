# Ruby - Binary
@Ruby

pack/unpack
-----------

### Integer

+-------------+--------------------------------------------------+
|Directive    | Meaning                                          |
+=============+==================================================+
|   C         | 8-bit unsigned (unsigned char)                   |
+-------------+--------------------------------------------------+
|   S         | 16-bit unsigned, native endian (uint16_t)        |
+-------------+--------------------------------------------------+
|   L         | 32-bit unsigned, native endian (uint32_t)        |
+-------------+--------------------------------------------------+
|   Q         | 64-bit unsigned, native endian (uint64_t)        |
+-------------+--------------------------------------------------+
|   c         | 8-bit signed (signed char)                       |
+-------------+--------------------------------------------------+
|   s         | 16-bit signed, native endian (int16_t)           |
+-------------+--------------------------------------------------+
|   l         | 32-bit signed, native endian (int32_t)           |
+-------------+--------------------------------------------------+
|   q         | 64-bit signed, native endian (int64_t)           |
+-------------+--------------------------------------------------+
|  S\_, S!    | unsigned short, native endian                    |
+-------------+--------------------------------------------------+
|  I, I\_, I! | unsigned int, native endian                      |
+-------------+--------------------------------------------------+
|  L\_, L!    | unsigned long, native endian                     |
+-------------+--------------------------------------------------+
|  Q\_, Q!    | unsigned long long, native endian (ArgumentError |
|             | if the platform has no long long type.)          |
|             | (Q\_ and Q! is available since Ruby 2.1.)        |
+-------------+--------------------------------------------------+
|  s\_, s!    | signed short, native endian                      |
+-------------+--------------------------------------------------+
|  i, i\_, i! | signed int, native endian                        |
+-------------+--------------------------------------------------+
|  l\_, l!    | signed long, native endian                       |
+-------------+--------------------------------------------------+
|  q\_, q!    | signed long long, native endian (ArgumentError   |
|             | if the platform has no long long type.)          |
|             | (q\_ and q! is available since Ruby 2.1.)        |
+-------------+--------------------------------------------------+
|   S> L> Q>  | same as the directives without ">" except        |
|   s> l> q>  | big endian                                       |
|   S!> I!>   | (available since Ruby 1.9.3)                     |
|   L!> Q!>   | "S>" is same as "n"                              |
|   s!> i!>   | "L>" is same as "N"                              |
|   l!> q!>   |                                                  |
+-------------+--------------------------------------------------+
|   S< L< Q<  | same as the directives without "<" except        |
|   s< l< q<  | little endian                                    |
|   S!< I!<   | (available since Ruby 1.9.3)                     |
|   L!< Q!<   | "S<" is same as "v"                              |
|   s!< i!<   | "L<" is same as "V"                              |
|   l!< q!<   |                                                  |
+-------------+--------------------------------------------------+
|   n         | 16-bit unsigned, network (big-endian) byte order |
+-------------+--------------------------------------------------+
|   N         | 32-bit unsigned, network (big-endian) byte order |
+-------------+--------------------------------------------------+
|   v         | 16-bit unsigned, VAX (little-endian) byte order  |
+-------------+--------------------------------------------------+
|   V         | 32-bit unsigned, VAX (little-endian) byte order  |
+-------------+--------------------------------------------------+
|   U         | UTF-8 character                                  |
+-------------+--------------------------------------------------+
|   w         | BER-compressed integer (see Array.pack)          |
+-------------+--------------------------------------------------+

### Float

| Directive | Meaning                                           |
|-----------|---------------------------------------------------|
| D, d      | double-precision, native format                   |
| F, f      | single-precision, native format                   |
| E         | double-precision, little-endian byte order        |
| e         | single-precision, little-endian byte order        |
| G         | double-precision, network (big-endian) byte order |
| g         | single-precision, network (big-endian) byte order |


### String

| Directive | Meaning                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------|
| A         | arbitrary binary string (remove trailing nulls and ASCII spaces)                                    |
| a         | arbitrary binary string                                                                             |
| Z         | null-terminated string                                                                              |
| B         | bit string (MSB first)                                                                              |
| b         | bit string (LSB first)                                                                              |
| H         | hex string (high nibble first)                                                                      |
| h         | hex string (low nibble first)                                                                       |
| u         | UU-encoded string                                                                                   |
| M         | quoted-printable, MIME encoding (:RFC:`2045`)                                                       |
| m         | base64 encoded string (:RFC:`2045`) (default)  base64 encoded string (:RFC:`4648`) if followed by 0 |
| P         | pointer to a structure (fixed-length string)                                                        |
| p         | pointer to a null-terminated string                                                                 |


### Misc

| Directive | Meaning                                         |
|-----------|-------------------------------------------------|
| @         | skip to the offset given by the length argument |
| X         | skip backward one byte                          |
| x         | skip forward one byte                           |



