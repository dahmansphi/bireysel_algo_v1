# About the Package
## Author's Words

Welcome to **the first Edition of the _Bireysel_ Algorithm** official documentation. I am Dr. Deniz Dahman 
the creator of the Bireysel algorithm and the author of this package. In the following section you 
will have a brief introduction on the principal idea of the Bireysel algorithm. 
In addition, a reference to the academic publication on the method. Before going ahead, I would like 
to let you know that I have done this work as an independent scientist without any fund or similar capacity. 
I am dedicated to proceeding and seek further improvement of the proposed method at all costs. 
To this end if you wish to contribute in any way to this work, please find further details  in the contributing section.  
  
## Contributing 

If you wish to contribute to the creator of this method and the author, you may want to check possible ways on: 

[patreon](https://patreon.com/user?u=118924481) 

[YouTube](https://www.youtube.com/@dahmansphi) 

If you prefer any other way of contribution, please feel free to contact me directly. Thank you

# Introduction

## The Bireysel Algorithm
Classification is something that exists in nature in a very mysterious way. In fact, I do believe that 
our evolution in some way is related to the __principle of classification__. See, we like to classify things,
sometimes, we use a set of **adjectives** e.g. the good one, the bad one, the far one the close one, etc. 
Other times, we intend to use a set of **nouns**, i.e. __classifying by group names__, e.g. the A group, 
the South way, etc. That’s weird itself, as I am trying to introduce the definition of classification, 
I did classify two ways already, as if **an infinite circle**. Anyway, see here are two ways we classify things, 
onc I called the subjective way of classification using **adjectives**, the second is objective way of classification using **nouns**. These are how society tends to use the principle of classifications using the human language.  
That has been said, there is this magical tool that uses its own independent language, tends to __dissolve__ this 
line of difference between **subjectivism**, and **objectivism**, and that is the use of **mathematics**. 
In mathematics, we tend to convert everything into set of numbers, yet to understand the _behavior_ and the _structure_
of those numbers, and finally, we just see how things are grouped.  
To this end, I introduce **a new method of classification** that is **Bireysel Algorithm**. _Bireysel_ in Turkish language it means **(individual, personal)**. The method is structured based on _three blocks_, 
- [x] the building block, 
- [x] the training block, 
- [x] and the prediction block.  

It basically, relays on **4 characteristics**, I call them _the personal profile_. To learn the details of this method please check out _the official academic publication_ found in the reference.   

## bireysel_algo_v1 package
As scientists we must be **skeptical**. Not in a destructive way but in a constructive way, so to speak. 
So, the best approach to be a constructive scientist is to build your research first in an **abstract way** 
then in a **concrete way**. To this end, I have proposed the method and its structure, yet, I had to introduce 
a _concrete_ measure on that proposal, and that is **the purpose of this package**. This package is the _first edition_
of the Bireysel Algorithm, official released name **bireysel_algo_v1**. This package will serve as a **testing** tool 
on the proposed method, of its first edition. In other words, **not yet for a production capacity**, but rather for 
**research and development** purposes ONLY. The essential finding on accuracy of prediction is _very much promising_. 
In future releases, enhancement of extra features will be added, and yet to be tested. 
To this end, you may feel free to follow the set-up instructions as the following sections suggest. 

# Installation 
> [!TIP]
> The first edition bireysel_algo_v1 is tested on several **problematic** datasets. What I mean by problematic is 
a dataset with **extreme overlapping behaviors** across classes and has **insufficient** classification **accuracy** 
using other classification methods. Those sets have various dimensions that go as high as _13000 observations_ 
and _36 variables_. I employed the method using a very **basic machine capacity** that today’s industry can offer. 
To conclude, you **don’t need any advanced hardware capacity** but only basic ones. 
In addition, you make sure you have Python 3 or above version.

## Install bireysel_algo
to install the package all what you have to do:
```
pip install bireysel-algo
```
You should then be able to use the package. You may want to confirm the installation

```
pip show bireysel_algo
```
The result then shall be as:

```
Name: bireysel_algo
Version: 2.0.0
Summary: TEST ON Bireysel METHOD FOR CLASSIFICATION PROBLEMS
Home-page: https://github.com/dahmansphi/bireysel_algo_v1.git
Author: Dr. Deniz Dahman's
Author-email: dahmansphi@gmail.com
```

## Employ the bireysel_algo

> [!IMPORTANT]
> It’s mandatory, to use the first edition of bireysel_algo, to make sure the training dataset meets the conditions: 
> 1. Number of observations > 40 per class 
> 2. Number of variables > 2 
> 3. Number of classes >= 2. 

> Once these conditions are met then you may employ the bireysel_algo. Anyway, the package has a condition built in to make sure those conditions are met. 

As I have mentioned in the introduction, there are **three blocks** for the bireysel_algo 
to make _the final prediction_. Essentially, we need a _training dataset_ that the package will **build**, 
then **train**. Eventually, we call on the **predict_test** to test the result. 
Since this is the **first edition** as a testing block for the method, you will see that 
the only _active_ function for prediction is **predict_test**. To this end you need to make sure:
> 1. The **training** dataset is separated from the class vector. i.e. you should have the ds and the cls. Where the shape of ds should be m x n and the cls should be m x 1  
> 2. The **test** dataset is separated from the class vector. i.e. you should have the ds_test and the cls_test. Where the shape of ds_test should be m x n and the cls_test should be m x 1. 

That all set and find, then follow the steps as:

- [x] create a training function
- [x] create a save model function
- [x] create a load model function
- [x] create a test model function

Lest's see each function in action:

### training functino
the training function expects **four args**:
1. the training ds
2. the training class vector
3. the radius number 0.1 <= r <= 0.99
4. number of report neighbors, assume 5 

Now, if **elements 3, and 4** sound foreign to you, you should read the academic publication on 
the method to understand their functions. Once that is done then you expect the function returns **instance** of the bireysel_algo that is **build and trained**. Technically speaking, that is **the model to save**. 

```
def train_bp_a(ds, cls, radius, report_num):
    '''this is the first main function on using this package, it expects 
    the ds, cls, and radius, and how many report you wish to see from the neighbors parameter. 
    it basically return the model for saving purpos
    '''
    inst = BireyselValue()
    inst.input_feature(ds=ds, cls=cls)
    inst.report_input()
    inst.build(radius=radius)
    inst.build_report(num=report_num)
    inst.train()
    inst.model_summary()

    return inst
```
### saving model function
This function will save the returned model from the training section. 
It expects two args and that is **the model** and the **path to save to**.

```
def save_model(inst,path_save):
    '''this function basically save the bp_a.v.1.0 model, requrist two args:
        1. the model to save that should be bp_a model instance
        2. the path of saving the model
    '''
    inst.save_model(file_name=path_save)
```
### loading model function
as the name suggests, we are going to load the model. the function expects ONE **arg**:
the **path to load from**, and it **returns that model**.

```
def load_model(path_load):
    '''this function basically load the bp_a.v.1.0 model and return it, requires the path of the model to load'''
    model_path = path_load
    model = BireyselValue()
    model.load_model(model_path=model_path)
    model.loaded_model_summary()
    return model
```

### testing prediction function
this is the final function to test the model. basically this function expects three args:
the **model** which has been loaded, the **test dataset**, and finally the **vector class**.
that is done then you feed all to the function, and you expect the result will be printed on the terminal.

```
def test_bp_a(model, ds_test, cls_test):
    '''this function execute the test on bp_a. requires:
        1. model
        2. ds test
        3. cls test
        both must be following the loaded model summary
    '''
    model.predict_test(input_test_feature=ds_test, cls_test_feature=cls_test)
```
Finally, you expected a printed report with accuracy on the terminal as:

```
__________________________________________
*****************END*********************************
predict by neighbors :*********************
[0.30769231 0.         0.69230769]
actul is  2 predict 2
__________________________________________
*****************END*********************************
predict by neighbors :*********************
[0. 0. 1.]
actul is  2 predict 2
__________________________________________
*****************END*********************************
predict by neighbors :*********************
[0.63636364 0.         0.36363636]
actul is  2 predict 0
__________________________________________
*****************END*********************************
 Your prediction test has accuracy of **94.73684210526315 %**, by neighbors:
```


# Future release 


# --- Library setup -----------------------------------------------------------

# When importing from the root of the unpacked tarball or git checkout,
# Python sees the "h5py" source directory and tries to load it, which fails.
# We tried working around this by using "package_dir" but that breaks Cython.
