type Equality : (a,a) -> Type where
  refl : (x,y) Equality
  
eq-sym : (x,y) Equality -> (y,x) Equality
refl eq-sym = refl
  
eq-trans : ((x,y) Equality,(y,z) Equality) -> (x,z) Equality
(refl,refl) eq-trans = refl
