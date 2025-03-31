# mermaid

Testing mermaid diagrams.

## How to show these diagram in Github

Unfortunately, Github does not support mermaid rendering natively. There is a [Chrome extension](https://github.com/BackMarket/github-mermaid-extension) by [Alex Mercier](https://github.com/amercier)

Check the discussion [here](https://stackoverflow.com/questions/50762662/how-to-install-mermaid-to-render-flowcharts-in-markdown)

Another solution in moving your repository to gitlab. It natively supports mermaid in all markdown files.

## Examples

### Flow

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

### Sequence

```mermaid
sequenceDiagram
Alice->>John: Hello John, how are you?
loop Healthcheck
    John->>John: Fight against hypochondria
end
Note right of John: Rational thoughts!
John-->>Alice: Great!
John->>Bob: How about you?
Bob-->>John: Jolly good!
```


### Gantt

```mermaid
gantt
section Section
Completed :done,    des1, 2014-01-06,2014-01-08
Active        :active,  des2, 2014-01-07, 3d
Parallel 1   :         des3, after des1, 1d
Parallel 2   :         des4, after des1, 1d
Parallel 3   :         des5, after des3, 1d
Parallel 4   :         des6, after des4, 1d
```

At leas in my case, all the diagrams from this one fail at rendering using the extensions. 

### Class

```mermaid
classDiagram
Class01 <|-- AveryLongClass : Cool
<<interface>> Class01
Class09 --> C2 : Where am i?
Class09 --* C3
Class09 --|> Class07
Class07 : equals()
Class07 : Object[] elementData
Class01 : size()
Class01 : int chimp
Class01 : int gorilla
class Class10 {
  >>service>>
  int id
  size()
}
```


### State

```mermaid
stateDiagram-v2
[*] --> Still
Still --> [*]
Still --> Moving
Moving --> Still
Moving --> Crash
Crash --> [*]
```


### Pie

```mermaid
pie
"Dogs" : 386
"Cats" : 85
"Rats" : 15
```


### User Journey

```mermaid
journey
    title My working day
    section Go to work
      Make tea: 5: Me
      Go upstairs: 3: Me
      Do work: 1: Me, Cat
    section Go home
      Go downstairs: 5: Me
      Sit down: 3: Me
```

## Using SVG

 Here we show in a standard format (SVG) without having to install any extensions. But we will have to create a process that automatically creates the images from the text.
