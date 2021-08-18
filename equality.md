```
{ Are-Equal : (B : Type) -> (A : Type) -> B -> A -> Type
; are-equal : (A: Type) -> (a : A) -> a (a (A (A Are-Equal)))
}

{ Are-Equal-Functions : (A : Type)
    -> (G : A -> Type) -> (F : A -> Type)
    -> ((a : A) -> a G) -> ((a : A) -> a F)
    -> Type
; are-equal-functions : (A : Type)
    -> (G : A -> Type) -> (F : A -> Type)
    -> (g : (a : A) -> a G) -> (f : (a : A) -> a F)
    -> ((a : A) -> a f (a g (a F (a G Are-Equal))))
    -> f (g (F (G (A Are-Equal-Functions))))
}

{ equal-functions-are-equal-as-functions : (A : Type)
    -> (G : A -> Type) -> (F : A -> Type)
    -> (g : (a : A) -> a G) -> (f : (a : A) -> a F)
    -> f (g (F (G Are-Equal)))
    -> f (g (F (G (A Are-Equal-Functions))))
; are-equal (f (g (F (G (A
    equal-functions-are-equal-as-functions)))))
    = (a |-> a f (a F are-equal)) (f (g (F (G (A are-equal-functions)))))
}

{ Are-Equal-Simple-Functions : (A : Type)
    -> (C : Type) -> (B : Type)
    -> (A -> C) -> (A -> B)
    -> Type
; f (g (B (C (A Are-Equal-Simple-Functions
    = f (g ((a |-> B) ((a |-> C) (A Are-Equal-Functions))))
}

{ are-equal-simple-functions : (A : Type)
    -> (C : Type) -> (B : Type)
    -> (g : A -> C) -> (f : A -> B)
    -> ((a : A) -> a f (a g (B (C Are-Equal))))
    -> f (g (B (C (A Are-Equal-Simple-Functions))))
; proof (f (g (B (C (A are-equal-simple-functions)))))
    = proof (f (g ((a |-> B) ((a |-> C) (A are-equal-functions)))))
}

{ congruence : (B : Type) -> (A : Type) -> (f : A -> B)
    -> (a-two : A) -> (a-one : A)
    -> a-one (a-two (A (A Are-Equal)))
    -> a-one f (a-two f (B (B Are-Equal)))
; are-equal (a-one (a-two (f (A (B congruence)))))
    = are-equal
}
```
