There are special terms
```
Path : (A : Type) -> A -> A -> Type
refl : (A : Type) -> (x : A) -> x (x (A Path))
path-induction : (A : Type) -> (C : (x : A) -> (y : A) -> y (x (A Path)) -> Type)
    -> ((x : A) -> x (A refl) (x (x C)))
    -> (x : A) -> (y : A) -> (p : y (x (A Path))) -> p (y (x C))
univalence : (A : Type) -> (B : Type) -> B (A Equivalence) -> B (A Path)
```

that satisfy
```
x (A refl) (x (x (c (C (A path-induction))))) = x c

```
