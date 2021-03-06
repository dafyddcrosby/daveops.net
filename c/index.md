---
title: C
---

## Resources

* <http://splint.org>
* <http://c-faq.com/>
* <https://www.securecoding.cert.org/confluence/display/c/SEI+CERT+C+Coding+Standard>
* [GCC non-bugs](https://gcc.gnu.org/bugs/#nonbugs_c)_
* <http://www.slideshare.net/olvemaudal/deep-c/24-What_will_happen_if_you>

## Misc Notes

* Don't cast returned pointers from malloc. (void \*) should get automatically promoted to any pointer type, and casting just makes it likely you'll get it wrong.
* Free allocated memory when you are done with it, don't assume that OS will clean up your mess.

## To verify

* ☐ C compiler will create implicit declaration of function, which can be satisfied at link time
* ☐ Difference between exit values in ANSI C, K+R, C99
* ☐ Are return values typically passed in a register?


