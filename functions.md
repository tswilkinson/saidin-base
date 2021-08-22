```
{ identity-function : (A : Type) -> A -> A
; a (_ identity-function) = a
}

{ compose-functions : (A : Type) -> (B : Type) -> (C : Type)
     -> (A -> B) -> (B -> C) -> A -> C
; a (g (f (C (B (A compose-functions))))) = a f g
}

{ Homotopy : (A : Type) -> (P : A -> Type)
    -> (f : (x : A) -> x P) -> (g : (x : A) -> x P) -> Type
; homotopy : (A : Type) -> (P : A -> Type)
    -> (f : (x : A) -> x P) -> (g : (x : A) -> x P)
    -> ((x : A) -> x g (x f (x P Path)))
    -> g (f (P (A Homotopy)))
}

{ is-equivalence : (A : Type) -> (B : Type) -> (f : A -> B)
    -> ((g : B -> A) -> f (g (B (A (B compose-functions)))) (A identity-function (
```
