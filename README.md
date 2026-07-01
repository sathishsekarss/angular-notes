# angular-notes
This Repository contains information related Angular concepts.

1. [Template interpolation in angular](#template-interpolation-in-angular)
1. [Directives in angular](#directives-in-angular)
    1. [Component directives in angular](#component-directives-in-angular)

## template-interpolation-in-angular
Template interpolation in angular means you can refer to the variables declared in .ts (component.ts) file.
eg:
```
{{totalCount}} -> Sample.component.html file
totalCount:number=50 -> Sample.component.ts file
```

## directives-in-angular
A directive is a class in Angular that extends the functionality of HTML elements by changing their behavior, structure, or appearance.

## types-of-directives-in-angular
In angular there are three types of directives
-  Component directives
-  Structural directives
-  Attribute directives

## component-directives-in-angular
In Angular, a Component is fundamentally a directive with a template. It is the most common type of directive and serves as the primary building block for creating user interfaces. Under the hood, Angular's @Component decorator extends the @Directive decorator to add template-oriented features.In Angular, a Component is fundamentally a directive with a template. It is the most common type of directive and serves as the primary building block for creating user interfaces. Under the hood, Angular's @Component decorator extends the @Directive decorator to add template-oriented features.

[Angular component directive example]("./assets/AngularComponentDirective.gif");
