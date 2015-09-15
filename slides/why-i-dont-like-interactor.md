##  Why I don&#39;t like Interactor

- Feels very loose
- Passing around a hash, not objects
- Ask, don't tell

note:
    While I like the idea of the interactor gem in theory, something about it feels wrong. It feels a bit loose and
    unstable, with different contexts getting in the way of one another the larger the organiser chain is. I'm also not
    entirely sure that it's actully object-oriented, as all you're doing it passing a generic context around. Also,
    nitpicky, but this is another Ask, don't tell solution.
