# Flowchart Examples

## Basic Syntax

```mermaid
flowchart
    a --- b
```

### Directions:

* TD / TB (default)
* BT
* RL
* LR

### Edges:

* `---`: solid
* `===`: thick
* `-.-`: dotted

Length: `----`

#### Arrows

* `-->`: Single arrow
* `<-->`: Double arrow

## Labels and Shapes

```mermaid
flowchart
    a[Hello] --- |SeaGL| b{2023}
```

Shapes:

* `[]`: Box
* `{}`: Diamond
* `(())`: Circle
* `[()]`: Database
* `>]`: Flag

## Full Example

```mermaid
---
title: Preparing a Talk
---
flowchart TD
    cfp>"See Announcement"]
    idea{"New idea for talk"}
    submit{submit}
    present((Present!))

    cfp --> idea

    idea --> |Good| submit
    idea -.-> |Meh| idea

    submit -.-> |Rejected| idea
    submit --> |Accepted| write

    subgraph write
        direction RL
        draft -->  slides
        slides --> practice
        practice --> reviewers
        reviewers --> draft
    end

    write ==> present
```
