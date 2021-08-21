There are special terms
```
Path : (A : Type) -> A -> A -> Type
refl : (A : Type) -> (x : A) -> x (x (A Path))
path-induction : (A : Type) -> (C : (y : A) -> (x : A) -> y (x (A Path)) -> Type)
    -> ((x : A) -> x (A refl) (x (x C)))
    -> (y : A) -> (x : A) -> (p : x (y (A Path))) -> p (x (y C))
ua : 
```

that satisfy
```
x (A refl) (x (x (c (C (A path-induction))))) = x c
```
