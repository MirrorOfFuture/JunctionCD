## greet
* greet
    - utter_answer_greet

## say affirm  with greet
* greet
    - utter_answer_greet
* affirm
    - utter_answer_affirm

## say affirm 
* affirm
    - utter_answer_affirm

## say no with greet
* greet
    - utter_answer_greet
* deny
    - utter_answer_deny

## say no 
* deny
    - utter_answer_deny

## say goodbye
* goodbye
    - utter_answer_goodbye

## thanks with greet
* greet
    - utter_answer_greet
* thanks
    - utter_answer_thanks

## thanks
* thanks
    - utter_answer_thanks

## who are you with greet
* greet
    - utter_answer_greet
* whoareyou
    - utter_answer_whoareyou

## who are you
* whoareyou
    - utter_answer_whoareyou

## who are you with greet
* greet
    - utter_answer_greet
* whoareyou
    - utter_answer_whoareyou

## what to do
* whattodo
    - utter_answer_whattodo

## what to do with greet
* greet
    - utter_answer_greet
* whattodo
    - utter_answer_whattodo

## what is overall status
* overall_status
    - utter_answer_overall_status
## what is the status with one wind generator
* one_wind_generator_status
    - utter_answer_one_wind_generator
## bug trouble shoot
* greet
    - utter_answer_greet
* overall_status
    - utter_answer_overall_status
* affirm
    - utter_answer_one_wind_generator
* affirm
    - utter_answer_replace_fan
* thanks
    - utter_answer_thanks

# predict future
* greet
    - utter_answer_greet
* future_predict
    - utter_future_predict
* affirm
    - utter_start_contingency_plan
* deny
    - utter_answer_deny
* thanks
    - utter_answer_thanks