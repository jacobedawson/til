I wanted to split a background on a single div into 2 separate areas, 1 a solid colour and the other transparent. This was to create a background for a header without having to create an additional div and play around with postioning (working with someone else's pre-existing code). 

The CSS linear-gradient did the trick: 

background: linear-gradient(180deg, #000 70px, rgba(255, 255, 255, 0) 0%);

This means that from top (180deg) I create a 70px solid background (black #000), while the rest of the div is a transparent block - but it has no width either (0%), so actually doesn't appear at all, yet doesn't mess with sizing either. 
