    There are only two hard things in Computer Science:

    cache invalidation and naming things.

    — Phil Karlton

We needed to find a good naming convention to prevent complexity and technical debt. this is how we scale our React large app.

Choosing or “creating” a naming convention is hard because:

- it should be understandable by everyone (no **EntityForListItem**)
- it should be simple to use (no **SimpleBeanFactoryAwareAspectInstanceFactory**)

Bringing these requirements to the technical level results in :

- making component responsibilities understandable in a glance
- describing the component “type”
- describing component module belonging
- making component easy to find (file name coherence)

Here how our naming convention works (well).
The convention

## $[Domain]|[Page/Context]|ComponentName|[Type]$

![1 -vlpNiogz2H6tYjF5NpHEw.png](/.attachments/1%20-vlpNiogz2H6tYjF5NpHEw-98a4ec2c-a941-4283-897e-d6ad84e85633.png)
Parts surrounded by “[]” are optional. ⤴️

## “The Domain”

    Which module of the system owns this component?
The domain basically refers to the product scope. In our case, when missing, this means that the component can be present in any module. It’s the case of the Sidebar or Navbar components.

## “The Page or Context”

    what is the parent component?
    which product subpart/page this component belongs to?

In case of a “root component” — a component without a parent, directly instantiated by a <Route> — we sometimes add the product page where this component is expected to be. In the other cases, if a component can be found in many “pages” of a product but only inside another component, we add a “Context”, basically the name of the parent component.

 If the component is nested in more than one other component, we only keep the closest one to avoid redundancy. Example: ChatConversationName is not SidebarChatConversationName. When missing, we expect to find this component at a “root level”.
## Component

The name of the component refers to its responsibilities, in short

    what does this component do?

The Sidebar component is a Sidebar. The ACommunityAddToShortListButton is a button component of ACommunity responsible for adding profiles to a shortlist. The ChatConversationName component is only responsible for displaying the name of a chat conversation.

## types

For now, we identified only 5 types of components:

    View component: only display a rendering of data (no API calls or internal actions)
    Button component: only display an actionable view
    Connect component: legacy connect components
    forms components: Input, Upload, etc …
    in case of HoC components, we add Component to the wrapped component, and the HoC take the original component name 
    This avoids the components consumer to know the underneath HoC complexity.

When missing, we assume that a component is a View component by default.
Last words

This convention will help us to grow our big SPA very fast without a coherence issue.