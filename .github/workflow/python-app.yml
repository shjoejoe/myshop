def dijkstra_two_stack(math_expr: str):
    """
    Evaluates parenthesised mathematical expression 
    """

    operator_stack = []
    value_stack = []
    accepted_operators = "+-*"

    # Loop over chars in expression
    for c in math_expr.strip():

        if c in accepted_operators:
            operator_stack.append(c)

        elif c.isnumeric():
            value_stack.append(int(c))

        elif c == ")":

            val = value_stack.pop()

            operator = operator_stack.pop()

            if operator == "+":

                val += value_stack.pop()

            elif operator == "-":

                val -= value_stack.pop()

            elif operator == "*":

                # FIXME: This should be multiplication!
                val /= value_stack.pop()

            value_stack.append(val)

    return value_stack.pop()
