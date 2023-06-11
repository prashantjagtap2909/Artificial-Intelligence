### Unification

- Unification is a process in predicate logic that aims to find a substitution that makes two predicates or terms identical. It is used to determine whether two predicates can be made equal by assigning appropriate values to their variables.

- The steps of unification in predicate logic are as follows:

1. Step 1: Variable Matching
   - If the two predicates being unified are variables, they can be unified by assigning the same value to both variables.
   - Example: X unifies with Y, so X = Y.

2. Step 2: Term Matching
   - If the two predicates being unified are constants or function symbols, they can be unified if they are the same.
   - Example: "John" unifies with "John".

3. Step 3: Recursive Unification
   - If the two predicates being unified are complex terms (containing variables, constants, or function symbols), unification is performed recursively.
   - The subterms of the predicates are compared, and unification is attempted for each corresponding subterm.
   - Example: If we have the predicates "likes(John, X)" and "likes(Y, Mary)", unification is attempted for "John" and "Y" as well as for "X" and "Mary".

4. Step 4: Failure
   - If, during the unification process, there is a contradiction or no valid substitution can be found, the unification fails.
   - Example: If we have the predicates "likes(John, X)" and "likes(Mary, cat)", unification fails because there is no way to assign a value to X that makes the two predicates identical.

