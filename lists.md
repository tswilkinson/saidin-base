```
{ List : Type -> Type
; empty-list : (A : Type) -> A List
; prepend-to-list : (A : Type) -> A -> A List -> A List
}

{ list-functor : List Functor
; list-functor = (map-list : (B : Type) -> (A : Type) -> (A -> B) -> A List -> B List |-> second-equality (first-equality (map-list (List Functor))))
}
```
