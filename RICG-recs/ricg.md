# TAG Recommenations to the RICG

On the 31st of May, Marcos Cáceres gave an overview to the TAG members of the
challenges being faced by the Responsive Images Community Group (RICG). 

## History  

Over the last two years, the RICG has been trying to solve the
problem of "responsive images": given a set of environmental and device
constraints (network type, device dimensions and pixel ratio), the user agent
should select an image most appropriate to present to an end-user. This work
grew out of much real-world experimentation within the Web Development community
to try to solve this problem with various hacks and polyfills (see [0] for an
overview of techniques currently used in the wild and pros and cons of each
approach). Given the limitations and issues with the techniques found in [0],
the Web development community got organized to try to work with browser makers
to come up with a "in browser" solution.

To inform the standardization process, the RICG produced a set of use cases and
requirements [1] and is working on a specification for a new `picture` element
destined for the HTML specification [2]. In parallel, as a response to the
demand for a solution from the RICG the WHATWG introduced a new attribute on the
`img` element called `srcset` [3]. As `srcset` did not  adequately meet the
RICG's use cases, the `picture` element builds on `srcset` to meet the goals
above.

## Challenges

Although this work has been going on for over a year, there has been little
traction from browser makers with regards to implementing either `picture` or
`srcset`. This has effectively paralyzed work on these specifications and left
the RICG in a state of dissolution. The RICG reached out to the TAG for guidance
on how to proceed forward.

## TAG Recommendations

1. The TAG recommends that the RICG continue to formalize and popularize
polyfills that meet their use cases, like 
[Picturefill](https://github.com/scottjehl/picturefill) (and not wait for browser 
makers to implement their specification). Reaching critical mass with polyfills
should help convince browser makers that a solution should indeed be standardized 
for the benefit of end-users, even if it takes a few more years.

2. The TAG recommends that the RICG discourage developers from directly using
the `<picture>` element or `srcset` on the Web before the solution is
standardized and widely available in browsers. This is to avoid conflicts. If
browsers do end up exposing srcset, they should only do so behind a user
settable flag until there is wide consensus that that is the right solution for
the Web platform.

3. The TAG recommends polyfilling a solution based on Web Components and
encourages the RICG to reach out to high profile polyfill implementations (e.g.,
x-tags and polymer) to have their solution integrated into those libraries. This
should assist with the proliferation of responsive images solutions in the
medium term.

4. Given 1 and 3, the RICG should continue to monitor usage of the solutions in
the wild and continue to refine their specification based on that.
Experimentation is critical to the refinement of a solution (see
http://extensiblewebmanifesto.org/).

## Links

[0] http://css-tricks.com/which-responsive-images-solution-should-you-use/ 
[1] http://usecases.responsiveimages.org 
[2] http://picture.responsiveimages.org 
[3] http://www.w3.org/html/wg/drafts/srcset/w3c-srcset/
