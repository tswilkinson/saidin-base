```
{ Functor : Type
; functor : (F : Type -> Type)
    -> (f : (B : Type) -> (A : Type) -> (A -> B)
        -> A F -> B F)
    -> ((A : Type) -> A identity (A (A f)) (A F identity ((A F -> A F) Path)))
    -> ((C : Type) -> (B : Type) -> (A : Type)
        -> (h : B -> C) -> (g : A -> B)
	-> g (h (A (B (C compose-simple)))) (A (C f))
	    (g (A (B f))) (h (B (C f))
	        (A F (B F (C F compose-simple))))
		    (C F (C F (A F
		        Are-Equal-Simple-Functions))))
    -> Functor
}

{ Map : Functor -> Type -> Type
; _ (_ (f (F functor))) Map = F
}

{ map : (f : Functor) -> (B : Type) -> (A : Type)
    -> (A -> B) -> A (f Map) -> B (f Map)
; _ (_ (f (F functor))) map = f
}

{ Natural-Transformation : Functor -> Functor -> Type
; natural-transformation : (g : Functor) -> (f : Functor)
    -> (n : (A : Type) -> A (f Map) -> A (g Map))
    -> ((B : Type) -> (A : Type) -> (h : A -> B)
        -> h (f map) (B n
	    (A (f map) (B (f Map) (B (g Map) compose-simple))))
	    (A n (h (g map)
	        (A (f Map) (A (g Map) (B (g Map) compose-simple))))
		(B (g Map) (B (g Map) (A (f Map)
		    Are-Equal-Simple-Functions)))))
    -> f (g Natural-Transformation)
}
```
