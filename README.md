## Indeterminate Checkboxes

You can view the demo for *this* repo at http://thenotary.github.io/IndeterminateCheckboxes/

For a working demo which served as the source of this repo, see https://css-tricks.com/examples/IndeterminateCheckboxes/

For a swell tutorial, see https://css-tricks.com/indeterminate-checkboxes/

When I went to the original tutorial, I couldn't just copy and paste the provided code into my existing app and have it work (because I was also running with a collapsible checkbox system and thus had a very messy markup schema)...
This codebase uses a really complicated recursion project (from the perspective of a backend ruby dev)
so I finally refactored the source tutorial code, and was then able to drop it into my web app.  
Bottom line, I'm sharing the cleaned up code (it's in a ruby-javascript dialect) so other's can re-use it with out spending too much time deciphering it and making adaptations.  

## Configuration

To use this code, set the class of all your checkboxes to be 'indeterminate-checkbox'.  

The default html markup scheme goes like this:

    ul
      li
        input.indeterminate-checkbox
        ul
          li
            input.indeterminate-checkbox

Notice that going from input up to li, it's just 1 step?  
That is defined as the variable at the top of the file `stepsFromCheckboxToContainer`.  
The `stepsFromContainerToParentContainer` refers to the distance from the deepest `li` to the next up `li`, 2 steps in this default scenario.  

Here are the default configuration settings:

    // Configs:
    var selectorForCheckboxes = 'input[type="checkbox"].indeterminate-checkbox',
        stepsFromCheckboxToContainer = 1,
        stepsFromContainerToParentContainer = 2;

## Usage

Simply call `IndeterminateCheckbox.init()` on a page you wish to have indeterminate, tree style checkboxes on.  

## License

This work was adapted from Chris Coyier.  You can see his license which applies to the revisions made to his code.  
https://css-tricks.com/license/
