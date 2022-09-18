

Riddle_classic of [can-you-cover-the-baking-sheet-with-cookies](https://fivethirtyeight.com/features/can-you-cover-the-baking-sheet-with-cookies/)
```python
import matplotlib
from matplotlib import pyplot as plt, patches

fig = plt.figure()
ax = fig.add_subplot()
def func_plot():
    alpha1 = 0.5 # np.random.randint(0, 10) / 10
    rect1 = patches.Rectangle((-0.50, -0.50), 1, 1, color='g', alpha = alpha1/5)
    #rect2 = patches.Rectangle((0, -0.50), 0.5, 1, color='red', alpha = 0.25)
    for a, b in zip([0, -.5, 0, .5, 0],[0.5, 0, 0, 0, -.5]):
        circle_ = patches.Circle((a, b), radius= 0.5, 
                                 color='m', alpha = alpha1 * .8)
        ax.add_patch(circle_)
    
    ax.add_patch(rect1)

ax = fig.add_subplot(111)
func_plot()
plt.xlim([-1, 1])
plt.ylim([-1, 1])
plt.axis('equal')
plt.grid()
```
![Plot](https://gist.github.com/jupihes/b475a0fd3efb91e063b81fffecb32209#file-plot_5c-svg)
https://gist.github.com/jupihes/b475a0fd3efb91e063b81fffecb32209#file-plot_5c-svg
