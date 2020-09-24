# floodgame_nonvr
This application uses the control treatment of the floodgame. It was developed as a control group for the floodgame in the VR lab. 
It does not include a question on presence and simulator sickness, and it contains flood risk perception and worry questions at the start. 
The experiment only includes survey questions that are part of the preregistration. This means that the following variables have been deleted (compared to `floodgame_online`): responsible, neighbors, independence, collectivism, numeracy, concern, probability_exact and beliefs.

To install the app to your local oTree directory, copy the folder 'floodgame_nonvr' to your oTree Django project and extend the session configurations in your ```settings.py``` at the root of the oTree directory:

```
SESSION_CONFIGS = [
    dict(
        name='floodgame_nonvr',
        display_name="Floodgame control group",
        num_demo_participants=1,
        app_sequence=['floodgame_nonvr'],
        demo=False,
        language='nl'
    )
                  ]
```

## Languages
* English 
* Dutch (through Django localization file)

Note that the understanding questions rely on [otree-utils](https://github.com/WZBSocialScienceCenter/otreeutils). 

## Issues
Localization was not stable for the *UnderstandingQuestionsPage*, which is why the questions have been translated manually. This issue should be solved if one wants to conduct an experiment simultaneously in two countries. 
