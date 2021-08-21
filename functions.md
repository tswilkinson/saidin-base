```
{ identity : (A : Type) -> A -> A
; a (A identity) = a
}

{ compose-simple : (C : Type) -> (B : Type) -> (A : Type)
     -> (B -> C) -> (A -> B) -> A -> C
; a (f (g (A (B (C compose-simple))))) = a f g
}
```
