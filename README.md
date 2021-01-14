# ytube-comments

Trying out different Natural Language Processing (NLP) techniques on YouTube comment data.

## Usage

1. Clone this repository using `git clone https://github.com/bonskotti/ytube-comments.git`
2. Access directory by `cd ytube-comments`
3. Open in [Jupyter Notebook](https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/execute.html) with `jupyter notebook youtube_comments.ipynb`

## Data
Downloaded from https://www.kaggle.com/nipunarora8/most-liked-comments-on-youtube

## What was done

1. Preprocessing of data
2. Applying different NLP tools 

 - Language detection
 - Extracting punctuation marks, stopwords
 - Most common words

3. Bag of Words
4. Fitting two regression models and predicting the amount of likes based on the content of the comment.

## Results

With NLP tools information about data was obtained, such as most common words. The prediction of likes based on the content of the comment does not work well, because possibly relevant data has been left out, such as the date and the names of the video and the channel. All of these are likely to have an impact on the view count of the video and thus on the amount of likes. These features were left out for simplicity. 

Of regression models, Support Vector Regressor gave a smaller MSE for predictions. However, it generally gave only small values for each comment where as Decision Tree Regressor's predictions had larger variations.

Next, the quantitative variable (likes) could be changed into a categorical one, and classification algorithms could be applied. Here again the variable's large variation would bring challenges on how to define the categories. One could also reduce the dimensions of the document-term-matrices and see whether it would improve the results.
