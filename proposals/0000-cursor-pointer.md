---
title: '`cursor` style property in React Native'
author:
- Vincent Riemer
date: today
---

# RFC0000: `cursor` style property in React Native

## Summary

Introduce the `cursor` property from the [web specification](https://drafts.csswg.org/css-ui/#cursor) with a particular focus on adding support for the `pointer` value.

## Basic example

```js
import { View, StyleSheet } from "react-native";

function CursorPointerExample() {
    return <View style={styles.example} />;
}

const style = StyleSheet.create({
    example: {
        cursor: "pointer",
    },
});
```

## Motivation

<!-- Why are we doing this? What use cases does it support? What is the expected outcome?

Please focus on explaining the motivation so that if this RFC is not accepted, the motivation could be used to develop alternative solutions. In other words, enumerate the constraints you are trying to solve without coupling them too closely to the solution you have in mind. -->

As we invest more in additional platforms such as VR, Desktop, and better Web interoperability — it has become clearer that React Native is lacking when it comes to first-class APIs for customizing the rendering of a platform's cursor. 

## Detailed design

This is the bulk of the RFC. Explain the design in enough detail for somebody familiar with React Native to understand, and for somebody familiar with the implementation to implement. This should get into specifics and corner-cases, and include examples of how the feature is used. Any new terminology should be defined here.

## Drawbacks

Why should we _not_ do this? Please consider:

- implementation cost, both in term of code size and complexity
- whether the proposed feature can be implemented in user space
- the impact on teaching people React Native
- integration of this feature with other existing and planned features
- cost of migrating existing React Native applications (is it a breaking change?)

There are tradeoffs to choosing any path. Attempt to identify them here.

## Alternatives

What other designs have been considered? Why did you select your approach?

## Adoption strategy

If we implement this proposal, how will existing React Native developers adopt it? Is this a breaking change? Can we write a codemod? Should we coordinate with other projects or libraries?

## How we teach this

What names and terminology work best for these concepts and why? How is this idea best presented? As a continuation of existing React patterns?

Would the acceptance of this proposal mean the React Native documentation must be re-organized or altered? Does it change how React Native is taught to new developers at any level?

How should this feature be taught to existing React Native developers?

## Unresolved questions

Optional, but suggested for first drafts. What parts of the design are still TBD?
