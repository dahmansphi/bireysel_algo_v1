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

# Future release 


# --- Library setup -----------------------------------------------------------

# When importing from the root of the unpacked tarball or git checkout,
# Python sees the "h5py" source directory and tries to load it, which fails.
# We tried working around this by using "package_dir" but that breaks Cython.
