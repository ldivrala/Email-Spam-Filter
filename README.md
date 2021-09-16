# Email Spam Filter

Dataset :: [Enron Email Dataset](https://www.cs.cmu.edu/~enron/ "Enron Email Dataset")

* Dataset :: 
  * This dataset was collected and prepared by the CALO Project (A Cognitive Assistant that Learns and Organizes).
  * Dataset is divided in folders according to spam and NonSpam.
  * This dataset contains many emails in text format with headers (To:, Cc:, Bcc:, Content-type: etc.).

* Inspiration::
  * Our aim was to try to analyze the dataset and try to figure out what factors are causes spam mails.
  * Predict email is spam or not with pytorch.
  * Is your email spam?
  
  
##### Steps (What we did)

- Data Cleaning :: 
  1. Find all the Headers and check needed headers(subject, from, content-type) for prediction.
  2. Replace tags, numbers, links, email address, headers with a name(`__tag__`, `HTTP_ADDR` etc. ).
  3. DataFrame Creation with filtered Content.

- Predication :: 
  1. Vocabulary creation with pytorch
  2. Email content encoding in vocab size array(Vocab word present == 1 or not == 0 in content).
  3. Creation of training and test data (Using only initial 700 rows). 
  4. Creation of Pytorch model with two Linear layers and training with train set.
  5. Testing and evalution (F1 Accuracy = 0.99295)
  6. Testing and evalution on 700 - 900 rows (F1 Accuracy = 1.0)

- Which words cause spam ::
  * Get model parameters and collect them by multiply in a array(size = vocab_size).
  * Finding word which cause spam.
 


