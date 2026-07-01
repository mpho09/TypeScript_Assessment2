 What does a generic constraint (`K extends keyof T`) buy you over `any`?
A generic constraint like K extends keyof T is better than any because it keeps your code safe by allowing only keys that actually exist on an object, while any removes TypeScript’s protection and allows mistakes that can only be discovered at runtime.

When would you use a mapped type vs a utility type like `Pick`?
You use a mapped type when you want to transform or modify the structure of an existing type, such as making all properties optional or readonly, while you use a utility type like Pick when you only want to select specific properties from an existing type without changing them.

What is the difference between `unknown` and `any`, and why is a type guard safer than a cast?
any means “TypeScript should not check this value,” so it gives you freedom but removes safety. unknown means “the type is not known yet” so TypeScript forces you to check the value before using it. A type guard is safer than a cast because a type guard actually verifies the type at runtime, while a cast only tells TypeScript to trust you without checking.

How does the `never` exhaustiveness check in the reducer protect you?
By making sure every possible action type is handled. If you add a new action but forget to update the reducer, TypeScript will warn you instead of allowing unexpected behavior.