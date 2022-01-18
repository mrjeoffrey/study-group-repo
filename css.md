// What is one commonly used technique to center a block element?

margin: 0 auto;

short hand for
margin-top: 0;
margin-bottom: 0;
margin-right: auto;
margin-left: auto;

// How do you create a sticky footer or header in css?
the parent element to stay in header or footer must have these two properties:

FOR HEADER
position: sticky;
top: 0;

FOR FOOTER
position: sticky;
top: 0;

// I'm always seeing different units being used to give something a size. What is the best recommended unit for different properties?

- all font-related properties, use pt.
- for sizing-related properties, use rem, or em.
- second best is using vh / vw.
- if you really don't care about mobile, tablet or if people have small desktop dimensions, use px. however you will need to use pt for fonts.

// what is a hexcode?

A unit for color. It is made up of 6 digits, which represent RGB so RRGGBB. The first two digits affect Red, second following affects Green, and last affects Blue. The range goes from 0 to F. 0123456789abcdef. F turns on the Hue, while 0 turns off. fo FFFFFF turns on all 3 RGB, and u get white. while 000000 turns off RGB and you get black. FF0000 turns on Red. 00FF00 turns on Green etc.
If you add another two digits, so that the total hexcode is 8, then you now have ability to play with opacity of that hexcode.