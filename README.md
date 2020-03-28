# Text-Sentimental-Analysis  
![7fb03628-d27f-4c3b-8eeb-8b48134fd25f](https://user-images.githubusercontent.com/3431730/77824022-5579dd80-7125-11ea-8470-770adbb4bdd9.jpeg)
## Vision of this code
This code is to analyse the behavior of text input by the user. Please see the following screenshots to know the things in more sense.    
**For positive text**
![positive_feeling](https://user-images.githubusercontent.com/3431730/43744997-3c4273bc-99fa-11e8-9169-2c10b311151e.png)
**For Negative text**
![negative_feeling](https://user-images.githubusercontent.com/3431730/43745028-659c4972-99fa-11e8-86a3-6a822ef95886.png)
**For Neutral text**
![neutral_feeling](https://user-images.githubusercontent.com/3431730/43745047-798c01de-99fa-11e8-9646-49d734f6355c.png)
## How I created database for this

<a href="http://positivewordsresearch.com/list-of-positive-words/" title="List of Positive Words">List of Positive Words are taken from this link</a>  
<a href="http://positivewordsresearch.com/list-of-negative-words/" title="List of Negative Words">List of Negative Words are taken from this link</a>  
Positve_words.xlsx file contains **614** rows while negative_words.xlsx contains **922** entries.

### What logic I applied
When any text is entered, it is convered into sentence and then to text using nltk module (sentence and words). Each word after tokenization is compared with the list of positive and negative words in the list and final answer is formed after below logic. You can change the logic according to your requirement.
```
        if positive_count >0 and negative_count ==0:
            print("Written text is postive and person is writing optimistic")
        elif negative_count>0 and positive_count == 0:
            print("Written text is negative and person is writing pessimistic")
        elif positive_count>negative_count and negative_count!=0:
            print("Person is writing more positive and less negative")
        elif negative_count>positive_count and positive_count!=0:
            print("Person is writing more negative and less positve")
        else:
            print("Person is writing neutral")
```            

### How to run the file
To run the file, please download both the xlsx files and text_analysis.py and put it into same folder. Now you need to give the path of the same folder either in the terminal or command prompt. This depends on whether you are using ubuntu or windows and run the follwing command.
```
python text_analysis.py
```
