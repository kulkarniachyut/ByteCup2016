# ByteCup2016
Competition-2016

Dataset provided in the competition contains three types of information:

  1、Expert tag data：which contains IDs of all expert users, their interest tags, and processed

profile descriptions.

  2、Question data：which contains IDs of all questions, processed question descriptions, question

categories, total number of answers, total number of top quality answers, total number of upvotes.

  3、Question distribution data：290,000 records of question push notification, each contains a

question ID, an expert ID and whether or not the expert answered the question. We will divide the

training set, validation set and test set based on these records.
 

 

  Please also note that:
 

  1、Training set is used for the training of the model. Validation set is used for online real-time

        evaluation of the algorithm. Test set is used for the final evaluation.

  2、All expert ID and question ID is anonymized to protect user privacy.

  3、Also for privacy protection purpose, we will not provide the original descriptions of the

        questions and the experts.Instead, we will provide the ID sequence of the characters (each

        Chinese character will be assigned an ID) and the ID sequence of the words after segmentation

        (each word will be assigned an ID). You are free to use either one or both.

  4、Validation and testing labels will not be published. The contest committee will use them for

        online evaluation and final evaluation only.  

 

  All data is included in two files in the following formats:

     user_info.txt: expert tag file

     Each line represents one expert user, which has four properties separated by /tab. The four

  properties are:

     1、Anonymized expert user ID: the unique identifier of each expert user.

     2、Expert user tags: there will be multiple tags, i.e. 18/19/20 may represent baby/ pregnancy/

           parenting.

     3、Word ID sequence: User descriptions (excluding modal particles and punctuation) are first

           segmented,then each word will be replaced by the Character ID, i.e.284/42 may represent

           "Dont Panic".

     4、Character ID sequence: User descriptions (excluding modal particles and punctuation) are first

           segmented, then each character will be replaced by the Character ID,i.e. 284/42 may represent

           “BE”.

     note:when a property is null we will use a placeholder "/" to represent it.

 

     question_info.txt: Question data file

     Each line represents one question, which has seven properties separated by /tab. The seven

  properties are:

     1、Anonymized question ID: the unique identifier of each question.

     2、Question tag: there will be single tags, i.e. 2 may represent fitness.

     3、Word ID sequence: User descriptions (excluding modal particles and punctuation) are first

           segmented, then each word will be replaced by the Character ID, i.e. 284/42 may represent

           “Dont Panic”.

     4、Character ID sequence: User descriptions (excluding modal particles and punctuation) are first

           segmented, then each character will be replaced by the Character ID, i.e.284/42 may

           represent “BE”.

     5、Number of upvotes: The total number of upvotes of all answers to this question. It may indicate

           the popularity of the question.

     6、Number of answers: The total number of answers to this question. It may indicate the popularity

           of the question.

     7、Number of top quality answers: The total number of top quality answers to this question. It may

           indicate the popularity of the question. 

     note:when a property is null we will use a placeholder "/" to represent it.

 

    The training set will contain one file with the following format:

    Invited_info_train.txt: Question distribution data

    Each line represents one question push notification record, which includes the encrypted ID of the

question, the encrypted ID of the expert user and if the expert user answered the question (0=ignored,

1=answered), separated by /tab.

 

    Validation set and test set will each contain one file (invited_info_validation.txt and 

    invited_info_test.txt) with the same format as the invited_info_train.txt. Each of the files will

contain a part of the push records.

