Karczmarz, Mukherjee, Sankowski, and Wygocki introduced a novel approach for feature attribution in machine learning algorithms based on decision tree structures.
Their proposed algorithm, TreeBANZ, presents an alternative to TreeSHAP, an existing feature attribution algorithm implemented in the well-known open-source library SHAP.
While the SHAP library utilizes the Shapley Value, a cooperative game theory tool that became popular to explain predictions of machine learning models, Karczmarz et al.'s. TreeBANZ algorithm advocates the utilization of another concept from cooperative game theory called the Banzhaf Value.

The authors demonstrated that TreeBANZ outperforms TreeSHAP in terms of computational complexity and numerical robustness, while yielding nearly identical results as far as the feature attribution is concerned.
However, the implementation of TreeBANZ and the accompanying experiments were conducted in an isolated environment, utilizing only a limited subset of SHAP functions and modifications for ease of use.
Consequently, the algorithm has not yet been integrated into an established machine learning library, hindering comprehensive experimental benchmarking against the TreeSHAP algorithm and its derivatives in real-world scenarios.

The primary contribution of our thesis will be the integration of the TreeBANZ algorithm into SHAP library itself.
Additionally, we will conduct an extensive analysis comparing TreeSHAP with TreeBANZ using selected datasets and tree ensembles.
Our implementation will offer notable advantages, including the evaluation and comparison of the newly proposed algorithm in real-life usage scenarios, rather than solely in isolated synthetic environments.
Furthermore, it will facilitate the widespread adoption of the TreeBANZ algorithm in new explainable artificial intelligence (XAI) projects by providing a publicly available Python package that seamlessly integrates with various tree ensemble libraries.
Moreover, users familiar with SHAP will find it easy to incorporate our implementation since it will be part of a TreeSHAP package fork.

The main challenge that we need to tackle involves implementing the TreeBANZ algorithm in a way that is integrated in a satisfactory way with the existing TreeSHAP implementation in the SHAP library.
In particular, we want the user to be able to transition smoothly from their existing solutions that is now based on TreeSHAP to our TreeBANZ.
Ideally, this should be possible only by just adjusting a set of parameters.
One specific technical challenge is that in the SHAP library, the Python layer communicates in a non-trivial way with C++ modules.
This will be also the case for TreeBANZ.

The structure of our thesis will be as follows: We will begin with a review of cooperative game theory approaches in the field of explainable artificial intelligence.
Next we will survey the most prominent and widely used decision tree ensemble structures, providing an overview of their characteristics.
Subsequently, we will describe the architecture and features of the SHAP library.
We will then present and analyze the implementation of Karczmarz et al.'s TreeBANZ algorithm within the SHAP library.
Following that, we will evaluate this implementation using various datasets and machine learning models, summarizing the results using plots and benchmark metrics.
Finally, we will draw conclusions from our tests and propose potential future research directions for further exploration of these findings.
