# DS-4002-Project-1
  This project utilizes topic modeling to investigate the top themes discussed in State of the Union addreses. It analyzes all State of the Union addresses as a whole, and also examines different eras in American history. The State of the Union Address is considered to be one of the most crucial tools for a president to set an agenda, shift public opinion, and reassure people in times of uncertainty [1]. It is the only time in any given year where the entire cabinet, every member of Congress, and supreme court gather in the same room. 
  The delivery of the State of the Union Address, previously called the Annual Message, has changed over the years [2]. In the 1790s, speeches were given before Congress. Thomas Jefferson then began the tradition of giving a written address which lasted until Woodrow Wilson [3]. The address further evolved as broadcasting and television provided an opportunity for the President to speak directly to the American people and rally support for his agenda [2]. 

## SRC 
### Installing/Building Code
  We accessed the data set through Kaggle and read it using Google Colab. The data set is a CSV file containing State of the Union addresses for the years 1790-2019. We utilized LDA and nltk packages to process the corpus. 
  We first removed punctuation and converted the text to lowercase. We then joined the text together into a string to create a word cloud of the most commonly used words in all of the addresses.  
  We used topic modeling to determine the top topics discussed for the addresses as a whole, and for eras of American history including the New Nation (1790-1815), Nation Expansion and Reform (1816-1860), Civil War and Reconstruction (1861-1877), the Rise of Industrial America (1878-1900), Progressive Era (1901-1928), Great Depression and World War II (1929-1945), and the Post War/Modern Era (1946-2019)[4]. Analysis of the State of the Union addresses as a whole and different eras allows us to make comparisons and account for changes.   
  For the entire corpus and for the different eras, we conducted the following process. First we tokenized the data to separate the sentences into words without punctuation. We then created a list of stop words to remove from the data set to improve the topic modeling. We then created a porter stemmer to account for variations in similar words. We then compiled the speech documents into a list and tokenized the speeches. Next, we cleaned and tokenized each document string, removed stop words from the tokens, stemmed the tokens, and then added the tokens to the list. Using this list, we turned our tokenized documents into an ID/term dictionary. We then filtered out extreme words to exclude tokens that appear in less than 5 speeches or in above 50% of speeches. We converted the tokenized documents into a document-term matrix. We used the corpus to geenrate the LDA model and found the top 3 topics from that corpus.  

### Usage of Code

  After generating the top topics for the corpus, we computed a coherence score to determine the usefulness of the output. We also computed perplexity, which is a measure of how good the model is. Finally, to get a better idea of the most frequently discussed topics, we created visualizations including an intertopic distance map to display any overlap in topics and its strength in the overall corpus. We also created a chart with the top-30 most salient terms used, which also indicates which words belong to which topic.  

## Data 

Data Dictionary
|Column Name|Definition                                                                                    |Data Type      | 
|-----------|----------------------------------------------------------------------------------------------|---------------|
|President  |Which president delivered the address                                                         |String         |
|Year       |Year the address was delivered                                                                |Integer        |
|Title      |Number address for the president that is delivering the address (ranges from first to twelfth)|String         |
|Text       |List of sentences containing the entire speech                                                |List of Strings|

[Link to data](Data/state_ofthe_union_texts.csv)

### Relevant Notes about the Use of Data
The data set was relatively small, which resulted in not a lot of data for the topic modeling to process. This is particularly important for the analysis of eras in American history, as shorter eras contained less data and therefore lower coherence scores in topic modeling.

## Figures 

## References
[1] A. Prokop, “The State of the Union Address’s history, explained,” Vox, Feb. 6, 2023. [Online]. Available: https://www.vox.com/2015/1/20/7854969/biden-state-of-the-union-address-history. [Accessed: Feb. 9, 2023].  
[2] “State of the union address: US House of Representatives: History, Art & Archives,” US House of Representatives [Online]. Available: https://history.house.gov/Institution/SOTU/State-of-the-Union/. [Accessed: Feb. 9, 2023].  
[3] R. Elving, “As the nation has changed, so has the State of the Union speech,” National Public Radio, Feb. 4, 2023. [Online]. Available: https://npr.org/2023/02/04/1154134314/state-of-the-union-address-2023-history. [Accessed: Feb. 9, 2023].  
[4]

### Links to MI1 and MI2
[MI1](https://docs.google.com/document/d/1-gNGJVQLpVzO9EekcbVrqv9PvzNYCDZYVpXvTuxJwJ8/edit?usp=sharing)  
[MI2](https://docs.google.com/document/d/1PZsgXShXIkSPw3CwpS5JDVV3jropM0ABtoxNYha5uuI/edit?usp=sharing)

