# Evolving NN

Author: Patrick Stetz  [(github)](https://github.com/pstetz/)

This is an idea for a NN architecture that I thought would be interesting.

### Premise

Neural Networks generally work better with more layers.  However adding more layers comes at the cost of expensive computation in backpropagation.  It doesn't make sense for a NN of 20 layers to take a dive into the data.  Learning everything at once maybe isn't the way to go.

### Idea

Instead of starting the Network to learn with a huge number of layers, start with a few.  This will be less likely to generalize and will be quicker computationally.  Monitor the error and check when it plateaus.

Once the accuracy plateaus, add another layer.  There are probably smart ways of doing this.  Freezing other layers for a bit so the new layer can learn.  Bringing other layers' values closer to zero, so they're easier to train.

The idea was to make this similar to transfer learning.  Humans can learn something completely new quickly because they already have experience with something familar.  In addition, people learn rough features first, then details, not everything at once.

### Issues

This may be just a roundabout way to the cost minimum.  Speed tests should reveal whether the learning happens quicker.

If the network is continued to evolve by adding and modifying layers, there will definitely be a lot of overfitting.

My laptop is pretty weak

I should get a job first