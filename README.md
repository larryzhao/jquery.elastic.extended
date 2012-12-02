#jquery.elastic.extended

jquery.elastic is an excellent jquery plugin made by Jan jarfalk, which provides the elastic functionality to a textarea.

When I use it in my project, I need to toggle a textarea between elastic and unelastic according to user's behavior, but 
the plugin doesn't provide a `unelastic` method, so I extended the original plugin a little bit, to provide a `unelastic`
method to clear things up.

It's based on the lastest version, `jQuery.Elastic 1.6.11`
 
##What I do
===
There are two things to do to unelastic a textarea:
* remove the hidden `div` created.
* unbind the corresponding event listeners.

#####Hidden Div
The textarea to be elasticed should have `id` attribute, the hidden `div` with the textarea id and a suffix `-elasticed`.
And when you call `unelastic` on the textarea, it will search for the `div` and remove it.

#####Unbind the corresponding event listeners
`keyup change cut paste resize update blur input paste` will be unbinded. 
