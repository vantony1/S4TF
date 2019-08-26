# Summary of work done during GSoC 2019


### Final Repository Link
``` https://github.com/param087/swiftML ```

### Final Report

During the summer 2019 Google Summer of Code, I worked with another GSoC participant P.Bhavasar to implement standard machine learning algorithms in swift for S4TF. 

I implemented the following algorithms:
```
- Decision Tree
- AdaBoost Classifier
- Gradient Boost Regressor
- Random Forest 
- XGBoost 
  (wrapper for the XGBoost library in Python)
- Support Vector Machine 
  (wrapper for libSVM library in C)
```
This is the link to my personal repo where I host all the work I have done: https://github.com/vantony1/S4TF

#### Flow of Progres

I started by working on the base decision tree algorithm; I used various academic books to further my understanding of decision trees and then implemented them to support growing trees with both info gain and gini impurity; Then, I implemented AdaBoost for Classification and Gradient Boost for Regression. Then, I moved on to implement Random Forest for both classification and regression problems. 

I started implementing SVM from scratch however found that the mathematics and the implementation very complicated; I was adviced to connect external libraries taking advantage of Swift language interoperability. That is exactly what I did to implement SVM through wrapping libSVM in swift. I had to edit a bit of the C code to make the connection work but 99% of the C code is as original. 

Lastly, I wrapped XGBoost library in swift to be used in S4TF.

I was documenting the code as I went along, however, I still had to go through and make sure the documentation was perfect in the end. I also made sure to follow the Google Swift Style guide.

I also made example end-to-end notebook for each of my algorithm implementations. They show you exactly how to use the library.

#### Work still to be done
1. the XGBoost library is very extensive; Currently, the wrapper is very basic and only support a small part of the wide functionality offered by the python library. I hope to continue working on expanding this functionality.
2. Merging SVM and XGBoost into the SwiftML master on param087's master branch was halted by Travis CI due to an unknown error; The algorithms themselves are working and have tested. This is probably a very niche issue and we will get it sorted out ASAP

### Final Thoughts

I learned a lot and grew as a student and programmer through this experience. I am looking forward to continue maintaining and growing this library.
