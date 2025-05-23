# POLICY ITERATION ALGORITHM

## AIM
Write the experiment AIM.

## PROBLEM STATEMENT
Explain the problem statement.

## POLICY ITERATION ALGORITHM
Include the steps involved in policy iteration algorithm

## POLICY IMPROVEMENT FUNCTION
### Name
### Register Number
Include the policy improvement function

## POLICY ITERATION FUNCTION
### Name:Jai Surya R
### Register Number: 212223230084

## OUTPUT:
```
def policy_iteration(P, gamma=1.0, theta=1e-10):
    random_actions = np.random.choice(tuple(P[0].keys()), len(P))
    # Write your code here to implement the policy iteration algorithm
    pi=lambda s:{s:a for s,a in enumerate(random_actions)}[s]
    while True:
      old_pi={s:pi(s) for s in range(len(P))}
      V=policy_evaluation(pi,P,gamma,theta)
      pi=policy_improvement(V,P,gamma)
      if old_pi=={s:pi(s) for s in range(len(P))}:
        break
    return V, pi
```
```
optimal_V, optimal_pi = policy_iteration(P)
```
```
print('Name:          JAISURYA         Register Number: 212223230084      ')
print('Optimal policy and state-value function (PI):')
print_policy(optimal_pi, P, action_symbols=('<', '>'), n_cols=7)
```
```
print('Reaches goal {:.2f}%. Obtains an average undiscounted return of {:.4f}.'.format(
    probability_success(env, optimal_pi, goal_state=goal_state)*100,
    mean_return(env, optimal_pi)))
```
```
print_state_value_function(optimal_V, P, n_cols=7, prec=5)
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/a4881cdb-dd5d-4559-b5ca-eb98a3b36213)


## RESULT:

Thus, the program to iterate Policy improvement and evaluation is implemented successfully
