# football-manager-ca-predictor

The ca_predictor is a sci-kit-learn model saved as a joblib file. 

```
 pip install joblib
```

### Required fields to run inference

```
['Corners', 'Crossing', 'Dribbling', 'Finishing', 'First Touch',
       'Free Kick Taking', 'Heading', 'Long Shots', 'Long Throws', 'Marking',
       'Passing', 'Penalty Taking', 'Tackling', 'Technique', 'Aggressiion',
       'Anticipation', 'Bravery', 'Composure', 'Concentration', 'Vision',
       'Decision', 'Determination', 'Flair', 'Leadership', 'Off The Ball',
       'Positioning', 'Teamwork', 'Work Rate', 'Acceleration', 'Agility',
       'Balance', 'Jumping Reach', 'Natural Fitness', 'Pace', 'Stamina',
       'Strength', 'Stability', 'Foul', 'diversity', 'Aerial Reach',
       'Command Of Area', 'Communication', 'Eccentricity', 'Handling',
       'Kicking', 'One On Ones', 'Reflexes', 'Rushing Out', 'Punching',
       'Throwing', 'GK', 'DL', 'DC', 'DR', 'WBL', 'WBR', 'DM', 'ML', 'MC',
       'MR', 'AML', 'AMC', 'AMR', 'ST', 'Left Foot', 'Right Foot']
```

### Load the ca_predictor file as a joblib file.

```
from joblib import load

model = load("./ca_predictor.joblib")
# The list is arranged in the same order as that in list above.
pred = model.predict(
    [
        [
            9,
            12,
            13,
            12,
            13,
            12,
            15,
            11,
            5,
            11,
            12,
            14,
            7,
            13,
            5,
            12,
            10,
            10,
            10,
            12,
            11,
            12,
            13,
            12,
            12,
            12,
            13,
            10,
            14,
            12,
            15,
            12,
            15,
            13,
            13,
            9,
            20,
            15,
            11,
            3,
            1,
            1,
            1,
            1,
            1,
            1,
            3,
            4,
            3,
            1,
            1,
            1,
            1,
            1,
            1,
            1,
            1,
            1,
            1,
            1,
            1,
            1,
            14,
            20,
            11,
            20,
        ]
    ]
)

print(pred)
```
