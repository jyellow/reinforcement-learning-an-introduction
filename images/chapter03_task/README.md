https://github.com/jyellow/reinforcement-learning-an-introduction/blob/master/chapter02/ten_armed_testbed.py#L241
执行
```python
    figure_2_3(runs=2000, time=500)
```

方法figure_2_3中epsilon均改为0.1用于控制变量。
https://github.com/jyellow/reinforcement-learning-an-introduction/blob/master/chapter02/ten_armed_testbed.py#L151-L164
```python
def figure_2_3(runs=2000, time=1000):
    bandits = []
    bandits.append(Bandit(epsilon=0.1, initial=5, step_size=0.1))
    bandits.append(Bandit(epsilon=0.1, initial=0, step_size=0.1))
    best_action_counts, _ = simulate(runs, time, bandits)

    plt.plot(best_action_counts[0], label='$\epsilon = 0.1, q = 5$')
    plt.plot(best_action_counts[1], label='$\epsilon = 0.1, q = 0$')
    plt.xlabel('Steps')
    plt.ylabel('% optimal action')
    plt.legend()

    plt.savefig('../images/figure_2_3.png')
    plt.close()
```
