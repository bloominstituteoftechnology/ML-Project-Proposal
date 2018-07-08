# ML Project Proposal
- Cassidy Dobratz
- MLSA18 Pass Prediction Challenge (https://dtai.cs.kuleuven.be/events/MLSA18/index.php)

## What track are you choosing (analysis or engineering)?
Analysis

## What is your data source?
The dataset is provided. Contains 12,124 passes performed during 14 different
games involving a Belgian football club during the 2014/2015 football season.

## Summarize the status of your data and what cleaning is needed.
Data is cleaned, but still needs time stamps transformed and sequenced. In addition
coordinates needs to be put in a workable format.

## Summarize the structure of your data and what models/techniques work with it.
The passes.csv file contains the dataset in a comma-separated format. The file contains 12,125 rows and 60 columns. In addition to a header row, the file contains one row for each pass providing the following information:

    time_start: pass made
    time_end: pass received
    sender_id: the identifier of the player who passed the ball;
    receiver_id: the identifier of the player who received the ball;
    x_*: the x coordinates of the locations of the players at the time of the pass;
    y_*: the y coordinates of the locations of the players at the time of the pass.




## What is your overall goal with this project?
To predict the receiver of a pass performed during a football match given the sender
of the pass as well as the locations of all the players on the pitch.

## Anything else you want to note about your project?
If it goes well I will write a follow up paper for submission to challenge.
