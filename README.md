# Action-wrapper

Hi, this is the description of one html/css pattern that makes it easy to disquise any one element with any other presentation. So you could style links as buttons, buttons as links, File inputs as checkboxes, radios as multiple select boxes… Wait, what?!

Ok, those examples are not that nice. However, using this pattern you could make links inside links, any custom checkboxes ot radios, even custom file inputs or selects (the last two cases would need a simple js to get the file's name or text of selected option).

## The concept

It's rather simple: you have the `controller` and the `view`. And a wrapper. the `controller` is a invisible block that is stretched over the wrapper. The `view` is anything that goes after the `controller`, so you could style it using the `+` selector and pseudoclasses on the `controller`.

## Semantics?

None of it. There are cases when you just need something, and there are ways to get it, ones — short, others — long. This is a shortcut, easy to understand and to use. But with a downside that is the lack of semantics.

However, you can try to solve this by adding the WAI-Aria's `role="presentation"` to the `view`. I hope this would somewhat help :)

Also, for better user experience, don't forget to add the `tabindex="-1"` to all the inputs and links (if you don't want to have them clickable) in the `view`.

## Enjoy!

You can view some examples here: http://kizu.github.com/Action-wrapper/

I'm planning to add more examples and to fix issues when they would appear.

Also, this method would work for IE too, however right now it won't :) I would fix it someday, or you can do this by yourself and send me a pull request, so you'll save me from running the VM and all this dirty work.