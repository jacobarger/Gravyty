# Code Reference Repo for Gravyty

Hi Jon / Gravyty Team! 

Most of my repositories are private due to them being private projects with intent to publish, part of an academic paper, or enterprise related, so I figured I would just create a reporsitory and throw a couple exercises which I have completed recently. 

I included five seperate projects in this repo, all in the google colab / jupyter format, though if you have any trouble with this format please let me know and I'm happy to quickly convert them to be pulled and executed in a local environment.

Two of these items I completed as part of my machine learning course, the SVM from scratch and statistical analysis. The comments are fairly detailed and can walk you through my thought process, I had a great deal of fun writing thme and that turned out to be one of my favorite courses (along with deep learning). 

The other three, are simple items I wrote for fun or to satisfy my own curiosity. Find a brief description of each below and let me know if you have any questions!

# Monty Hall Problem 
If you haven't heard of the problem, it is a simple execrise wherein you are given three doors, one with a prize and two with something you wouldn't want, say a rock. If you pick a door, and the person conducting the exercise reveals one of the doors you did not pick to have a rock behind it, and then asks you if you would like to switch doors. Should you switch to the other door that you did not pick? The answer is statistically yes, if you switch, 66% of the time you will win the prize. 

After describing this problem to my family, we reached an impass in terms of them believing the idea that you should always switch when given the choice. Therefore I wrote a small script to play the situation, and then automate the decision process randomly 100000 times, in order to show the vast disparity in winning probability when switching.

# Similarity (Text Similarity)
I was given the prompt to write a novel method of calcualting the similarity of strings, with the caveat that it does not have to be optimal / perform extremely well. So this was more of a creativity exercise. Since 'similarity' is somewhat ambiguous, my goal became to focus less on words and implement a method which factors in character proximity when checking for similarity. By this I mean that 'abc' is much more similar to 'cab' than 'zxy' because of the letter's proximity to each other lexicographically. The way I handled this was by coverting all of the characters (including punctuation) into their ASCII equivelants, and then converting that into an array. I then pad the arrays with average values for that array (I know, this is very unpractical but fun for the purposes of this exercise). With these averages I calculate the cosine similarity, which accounts for proximity due to the numerical conversion, but due to the unscaled nature of punctuation as ASCII values, and the fact that this is case sensitve, the accuracy is fairly unreliable. Though this could definitely be improved in terms of accuracy by disregarding punctuation and casing.

As a final fun exercise, I wanted to represent similarity graphically. To do this, I took my arrays created in the steps above and plotted the lines over top of each other, this way you can look and see that when two strings are identical, they overlap perfectly. The huge spikes in this graphical representation (check out the example below) depict the punctuation, as the ASCII values for punctation are quite far from the ASCII values for letters.

# Point Position Classifier
This was done at an airport to occupy my time, hence the code / comments are a bit more sparse. The idea here was to fill up a predefined area with a bunch of randomly placed points, and then randomly create a box somewhere inside that area. We can then feed that information into a machine learning model (an SGD classifier) by dividing the points into two binary classes, inside the box or outside. The features are the coordinates of the points. The model then is given a different test set of points, and has to tell me if the points are inside the box or not. Note that the machine learning model has no idea where the box is or what its coordinates are. 

