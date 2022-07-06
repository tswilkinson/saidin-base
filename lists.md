type List : Type -> Type where
  nil : a List
  cons : (a,a List) -> a List

