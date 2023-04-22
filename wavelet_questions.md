### Section 4.1

1) Do you know if there is any good "visual" explanation of the graph Laplacian's spectrum and a graph Fourier transform?

2) What is the meaning of the chosen heat kernel in that section? How is diffusion and heat kernel defined on a graph?

3) If we have a wavelet on a signal in time, it lives in the signal's frequency domain and in time (?)\
If we have a wavelet on an image, we would operate with a signal with frequences in one dimention of the image and their localization in another dimension of the image (?)\
If we have a wavelet on a graph, it lives in the spectral domain, but what is the "time" part of the wavelet in that case?

4) What is "scale $s$"? Is it that "time" thing? Is $s$ an integer given that we have it both in the heat kernel and in index? For example, in each $g()$, i.e. in $\Sigma_s=diag(g(s\lambda_1),....,)$?\
Connecting it to the Question 1), why "a node’s neighborhoods can be adjusted by varying the scaling parameter $s$"?

5) We have $\psi_s=(\psi_{s,i}),~i=1...n$. Our "frequencies" are n ones corresponding to each eigenvector/eigenvalue. Since we have index i in each psi, does it mean we have a wavelet component for each eigenvalue?...\
What is a wavelet, $\psi_{si}$ or $\psi_{s}$?\
What is a "mother wavelet"?

6) $L = U\Lambda U^{-1}=U\Lambda U^T$ (since U is orthonormal?)\
Then, $\psi_s=U\Sigma_sU^T$.\
What's the relation between $\Lambda \text{ and } \Sigma_s$?\
Intuitively, I thought that $\Sigma_s$ a filter that we apply to the spectrum of a graph. So in my mind it kind of already has the meaning of a wavelet. But then I don't fully get what $\psi_s$ is.
Or do we just need $U$ to define anything that lies in the spectral domain of our graph??

7) Connected to Q 1), 6).\
If I have 2 graphs of, say, 8 and 15 nodes that share the same substructure (for example, c1nc(C)nc1, what would be the relation between their spectra?\
If I generate a wavelet with low $s$ that is localized on an atom of this 5-membered ring substructure, for each graph it will be defined through their spectra which are different. (?)\
Then how do I learn that for different graphs this wavelet is localized on the same substructure?

### Section 4.2

8) Didn't fully get what happens when we contract one of the dimenstions of the tensor.

### Other questions for Section 4
9) Is the depth of positional encoding given by $K$?
10) I always took it for granted that we can use things coming from the graph spectrum as positional encodings, but (Q 1) I don't get how can eigenvectors of two different graphs of different sizes be related at all?
11) Do the matrices we learn during training have the number of nodes' dimension $N$ inside of them or not? (I didn't fully understand what exactly do we learn)

### Section 5.2
12) Is the number of clusters $C$ a fixed hyperparameter? (At least in the cited Ying et al, 2018, it was a fixed hyperparameter). 
13) What happens if we train a model on large molecules with $C$ selected to match them and then run it on a small molecule? Will we get repeated clusters? 
14) I hoped so much that they get clustering somehow directly from the atom embeddings without explicit clustering step :( :( :( I thought that a wavelet itself defines a substructure in the molecule... :(

### Results
15) From Fig. 5 and 4, I am actually not persuaded that the model learnt anything very meaningful about functional groups and clustering... Learning that NH3+ terminal group or a part of a 5-membered ring (not even the whole one) is a separate cluster doesn't look like a big deal.... Interesting that in the peptide case, it didn't learn the backbone as something separate.
16) Same for the T-SNE -- it is expected to see some separation in the results of a well-performing model... But they don't really explain the clusters...

### Other questions
17) How numerically stable are networks that have eigenvector/eigenvalaue computations in them? Is it ok to use float32 in them?
