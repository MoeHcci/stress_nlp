<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NLP Model For Human Stress Prediction</title>

<style>
        h1 {
            text-align: center;
        }

        table,
        th,
        td {
            border: 1px solid black;
        }
</style>

    
</head>

<body>
    <div>
        <h1>
            NLP Model For Human Stress Prediction
        </h1>
    </div>

    <div>
        <h2>General Information About The Project: </h2>
    </div>
    <div>
        <ul>
            
            <li>The project is written in Python in a Jupyter Notebook format</li>
            <li>The motivation behind the dataset is to produce a machine learning model that can predict if an individual is suffering from a psychological stress or not </li> 
            <li>The dataset behind the project is captured from multiple subreddits and is available at the following link from kaggle.com <a
                href="https://www.kaggle.com/datasets/mirichoi0218/insurance"> DataSet Link
                </a>  
            <li>The project initially starts by conducting EDA and producing a ml_nlp.csv file from the test_preprocessing.ipynb file</li>
            <li>The second part of the project takes the produced CSV file from the text preprocessing step and conducts an ML analysis on the data in the maincode.ipynb file</li>
            <li>Detailed work of preporcessing the data is available at <b>test_preprocessing.ipynb</b></li>

            <li>Detailed work of applying each algorithm is available at <B>maincode.ipynb</B></li>




        </ul>
    </div>



    <div>
        <h2>EDA Conclusions Written Information: </h2>
    </div>
    <div>
        <ul>
            <li>There is a total of <b>7</b> features which are: </li>
            <ul>
                <li><b>subredit</b>, the subreddit the text comes from </li>
                <li><b>post_id</b>, the post's id </li>
                <li><b>sentence_range</b>, the size of the sentence</li>
                <li><b>text</b>, the text that will represent the state of the person</li>
                <li><b>label</b>, this is the label feature column that indicates if a person is going through psychological stress or not. The value of 1 means the person is going through psychological stress. The value of 0 means the person is not going through psychological stress </li>
                <li><b>confidence</b>, this is the confidence level of person on text</li>
                <li><b>social_timestamp</b>, this is the social timestamp </li>
               
            </ul>

            <li>The project focused on two features. The <b>text</b> feature which was the input feature and the <b> label</b> feature which was the output feature</li>


        </ul>

    </div>





    <!-- <div>
        <h2>Main Metrics of Evaluation: </h2>
    </div>
    <div>


    </div> -->

<div>


            <h2>Comparison  of the Algorithms Table: </h2>

            <ul>
                <li>For each of the algorithms analyzed the Accuracy and Recall</li>
                <li>The NLP study had two major goals. The best is producing an algorithm with good accuracy. The second is to decrease the false negative, which means we predict a person has no psychological issues while they do. The best metric to decrease false negatives tends to be recall</li>
    
    
            </ul>


            <table style="width:80%">
            <tr>
            <td><b>Algorithm</b></td>
            <td><b>False Negative</b></td>
            <td><b>True Positive</b></td>
            <td><b>True Negative</b></td>
            <td><b>False Positive</b></td>
            

            <tr>
                <td><b>Logistic Regression - Metric = Accuracy = 74% </b></td>
                <td>68 </td>
                <td>183 </td>
                <td>240 </td>
                <td>77 </td>

                
                </tr>


            </tr>
            

            

            </tr>
            <tr>
            <td><b>Logistic Regression - Metric = Recall = 99% </b></td>
            <td>0 </td>
            <td>27 </td>
            <td>308 </td>
            <td>233 </td>

        
            
            
            <tr>
            <td><b>Multinomial Naive Bayes - Metric = Accuracy =71% </b></td>
            <td> 54 </td>
            <td> 155  </td>
            <td>   254</td>

            <td>  105 </td>

            
            
            </tr>
            

            
            <tr>
            <td><b>Multinomial Naive Bayes - Metric = Recall = nan</b></td>

            <td>21 </td>
            <td>120 </td>
            <td>287 </td>
            <td>140 </td>

            
            
            </tr>
            

            <tr>
                <td><b>Bernoulli Naive Bayes - Metric = Accuracy - 73% </b></td>
                <td> 42 </td>
                <td> 157 </td>
                <td>   266</td>
                <td> 103 </td>

                
                
                </tr>
                

                
                <tr>
                <td><b>Bernoulli Naive Bayes - Metric = Recall = nan </b></td>
    
                <td>16  </td>
                <td>120  </td>
                <td>292</td>
                <td>140 </td>

                
                
                </tr>











    
            
            </table>


 </div>


 <h2>Conclusions: </h2>

 <ul>
     <li>      The algorithm with the highest accuracy is logistic regression at 74%. However, the other two algorithms have a very close values for accuracy at 71% for Multinominal Naïve Bayes and 73% for Bernoulli Naïve Bayes 
    </li>
     <li>     Both Naïve Bayes algorithms did not converge when their metric was set to “recall” and while using RandomizedSearchCV or GridSearchCV. Therefore, to solve for that we use a trail and error method by tuning the alpha smoothing parameter values until we achieved a satisfactory alpha value that produced low False Negatives and did not decrease the True Positives by too much
    </li>
     <li>       Based on the results of the algorithms the best performing algorithm is the Bernoulli Naïve Bayes with an alpha of 3, because it produced a low False Negative and an acceptable value of True Positives. Even though Logistic Regression with recall as the metric produced 0 False Negatives but it resulted in a very low value for the True Positives 
    </li>

     
 </ul>
































</body>

</html>
