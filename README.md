# News_Classification_Gensim
I gonna use pre trained word2vec model to preprocess the text and vectorize it
# First I gonna use "gensim.downloader" and load word2vec model trained on google news and check class balance in my dataset, my data in almost perfect
# Then I change label column into numeric values mapping label column into 0 and 1 and check change in my dataset
# Next I load large eanglish model from spacy, It is trained on huge dataset
# Now I gonna define function that will preprocess and vectorize my whole dataset
# So first I put my text into nlp object, then I create empty list for my new text already tokenized, preprocess and vectorized
# Then I make for loop on every token in my nlp object, it will be skipping stopwords and punctuation words
# So I set continue to ignore them and list will be filling with Lemmatized tokens, so  base forms of tokens
# And I apply on my filtered_tokens "get_mean_vector" function, its function from my model, "preprocess_and_vectorize" function will return me exzactly this
# Now I check samples, what I get from my function before vectorization and after vectorization and check shape of it
# I gonna create new column based on my "Text column", so I use function apply and lambda to apply "preprocess and vectorize" function on my "text"
# Then I import "train_test_split" and get train and test set and stratify my "y" to get equal number of samples 
# Next I gonna stack my X_train and X_test to convert it into 2d object, so I create new variable and show results
# Then I import "GradientBoostingClassifier" and "classification_report", create object of my class, train it with my data and get y_pred 
# I put true and y_pred data to my "classification report" and get results, score of true and predicted class are very high
# I don't need to change my classifier 
# Now I gonna take some samples from my data and store it into variable text, then I use "preprocess_and_vectorize" function on it and predict results
# My model work very good
# Then I gonna import "confusion_matrix" and look at results, diagonal values are good predictions, everything is alright 
# I also gonna plot my "confusion_matrix" for more visuality, so I import "pylot" and "seaborn", set size of of images 
# Then I supply "confusion_matrix" results, named labels and I look what I get, black squares are false predictions and bright are correct predictions
