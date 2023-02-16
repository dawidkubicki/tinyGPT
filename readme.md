Inspiration video: https://www.youtube.com/watch?v=kCc8FmEb1nY&ab_channel=AndrejKarpathy
Colab file: https://colab.research.google.com/drive/1JMLa53HDuA-i7ZBmqV7ZnA3c_fvtXnx-?usp=sharing#scrollTo=h5hjCcLDr2WC

# Day 1

File url: https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt

1. Read tinyshakespeare txt file
2. Analyse it
    1. Length
    2. Look at first 1000 chars
    3. Look at unique chars
3. Make a var called vocab_size
    1. Print chars from vocab (''.join(chars))
4. Create encode and decode functions (char2idx and idx2char)

# Day 2

1. Let's now encode the entire text dataset and store it into a torch.Tensor (type long)
2. Print shape, dtype, and first 1000 elements
3. Let's now split up the data into train and validation sets - first 90% will be train, rest val
4. Create a single training input with block size of 8 elements
5. Recreate something like this: 

when input is tensor([18]) the target: 47
when input is tensor([18, 47]) the target: 56
when input is tensor([18, 47, 56]) the target: 57
when input is tensor([18, 47, 56, 57]) the target: 58
when input is tensor([18, 47, 56, 57, 58]) the target: 1
when input is tensor([18, 47, 56, 57, 58,  1]) the target: 15
when input is tensor([18, 47, 56, 57, 58,  1, 15]) the target: 47
when input is tensor([18, 47, 56, 57, 58,  1, 15, 47]) the target: 58 

6. Recreate the same as above but with batches (batches - number of sequences processed in parralel) 