### IBM Cloud API

**Personality Insight API:** 

- Request url: <https://watsonchatcharbot.eu-gb.mybluemix.net/pi> 
- Request method: **POST**/GET 
- Sample code (python):

```python
import requests;
import json

data = {
    "text": "I am happy to join with...we are free at last!(content)"
}
url="https://watsonchatcharbot.eu-gb.mybluemix.net/pi"
response = requests.post(url, data)

# byte to string
result = response.content.decode("utf-8")
# string to json
result_json = json.loads(result)
# formatting
print(json.dumps(result_json, indent=4))


```

- Output:

```python
Analysis link: https://console.bluemix.net/docs/services/personality-insights/output.html#output
{
    "word_count": 1654,
    "processed_language": "en",
    "personality": [
        {
            "trait_id": "big5_openness",
            "name": "Openness",
            "category": "personality",
            "percentile": 0.9967728266376712,
            "significant": true,
            "children": [
                {
                    "trait_id": "facet_adventurousness",
                    "name": "Adventurousness",
                    "category": "personality",
                    "percentile": 0.7785746909381513,
                    "significant": true
                },
                {
                    "trait_id": "facet_artistic_interests",
                    "name": "Artistic interests",
                    "category": "personality",
                    "percentile": 0.999026769138005,
                    "significant": true
                },
                {
                    "trait_id": "facet_emotionality",
                    "name": "Emotionality",
                    "category": "personality",
                    "percentile": 0.8286509446973389,
                    "significant": true
                },
                {
                    "trait_id": "facet_imagination",
                    "name": "Imagination",
                    "category": "personality",
                    "percentile": 0.6226124525420123,
                    "significant": true
                },
                {
                    "trait_id": "facet_intellect",
                    "name": "Intellect",
                    "category": "personality",
                    "percentile": 0.9987376646674385,
                    "significant": true
                },
                {
                    "trait_id": "facet_liberalism",
                    "name": "Authority-challenging",
                    "category": "personality",
                    "percentile": 0.7476607191901985,
                    "significant": true
                }
            ]
        },
        {
            "trait_id": "big5_conscientiousness",
            "name": "Conscientiousness",
            "category": "personality",
            "percentile": 0.9668436373993838,
            "significant": true,
            "children": [
                {
                    "trait_id": "facet_achievement_striving",
                    "name": "Achievement striving",
                    "category": "personality",
                    "percentile": 0.8371428897304272,
                    "significant": true
                },
                {
                    "trait_id": "facet_cautiousness",
                    "name": "Cautiousness",
                    "category": "personality",
                    "percentile": 0.9468658014233253,
                    "significant": true
                },
                {
                    "trait_id": "facet_dutifulness",
                    "name": "Dutifulness",
                    "category": "personality",
                    "percentile": 0.8860741769595435,
                    "significant": true
                },
                {
                    "trait_id": "facet_orderliness",
                    "name": "Orderliness",
                    "category": "personality",
                    "percentile": 0.8139759716635869,
                    "significant": true
                },
                {
                    "trait_id": "facet_self_discipline",
                    "name": "Self-discipline",
                    "category": "personality",
                    "percentile": 0.7736496027999435,
                    "significant": true
                },
                {
                    "trait_id": "facet_self_efficacy",
                    "name": "Self-efficacy",
                    "category": "personality",
                    "percentile": 0.7697324754834105,
                    "significant": true
                }
            ]
        },
        {
            "trait_id": "big5_extraversion",
            "name": "Extraversion",
            "category": "personality",
            "percentile": 0.116232161027227,
            "significant": true,
            "children": [
                {
                    "trait_id": "facet_activity_level",
                    "name": "Activity level",
                    "category": "personality",
                    "percentile": 0.8979927186538061,
                    "significant": true
                },
                {
                    "trait_id": "facet_assertiveness",
                    "name": "Assertiveness",
                    "category": "personality",
                    "percentile": 0.792391913893333,
                    "significant": true
                },
                {
                    "trait_id": "facet_cheerfulness",
                    "name": "Cheerfulness",
                    "category": "personality",
                    "percentile": 0.4620982904129578,
                    "significant": true
                },
                {
                    "trait_id": "facet_excitement_seeking",
                    "name": "Excitement-seeking",
                    "category": "personality",
                    "percentile": 0.36915923232696457,
                    "significant": true
                },
                {
                    "trait_id": "facet_friendliness",
                    "name": "Outgoing",
                    "category": "personality",
                    "percentile": 0.7166558548039512,
                    "significant": true
                },
                {
                    "trait_id": "facet_gregariousness",
                    "name": "Gregariousness",
                    "category": "personality",
                    "percentile": 0.18830781773586264,
                    "significant": true
                }
            ]
        },
        {
            "trait_id": "big5_agreeableness",
            "name": "Agreeableness",
            "category": "personality",
            "percentile": 0.3133428942577051,
            "significant": true,
            "children": [
                {
                    "trait_id": "facet_altruism",
                    "name": "Altruism",
                    "category": "personality",
                    "percentile": 0.9661320986974831,
                    "significant": true
                },
                {
                    "trait_id": "facet_cooperation",
                    "name": "Cooperation",
                    "category": "personality",
                    "percentile": 0.8373777962626504,
                    "significant": true
                },
                {
                    "trait_id": "facet_modesty",
                    "name": "Modesty",
                    "category": "personality",
                    "percentile": 0.8583723242483969,
                    "significant": true
                },
                {
                    "trait_id": "facet_morality",
                    "name": "Uncompromising",
                    "category": "personality",
                    "percentile": 0.9199711263473,
                    "significant": true
                },
                {
                    "trait_id": "facet_sympathy",
                    "name": "Sympathy",
                    "category": "personality",
                    "percentile": 0.9989895870381571,
                    "significant": true
                },
                {
                    "trait_id": "facet_trust",
                    "name": "Trust",
                    "category": "personality",
                    "percentile": 0.8243619732320313,
                    "significant": true
                }
            ]
        },
        {
            "trait_id": "big5_neuroticism",
            "name": "Emotional range",
            "category": "personality",
            "percentile": 0.903842118128368,
            "significant": true,
            "children": [
                {
                    "trait_id": "facet_anger",
                    "name": "Fiery",
                    "category": "personality",
                    "percentile": 0.01895604740341028,
                    "significant": true
                },
                {
                    "trait_id": "facet_anxiety",
                    "name": "Prone to worry",
                    "category": "personality",
                    "percentile": 0.12781746653678344,
                    "significant": true
                },
                {
                    "trait_id": "facet_depression",
                    "name": "Melancholy",
                    "category": "personality",
                    "percentile": 0.34877288696248643,
                    "significant": true
                },
                {
                    "trait_id": "facet_immoderation",
                    "name": "Immoderation",
                    "category": "personality",
                    "percentile": 0.05727479982291389,
                    "significant": true
                },
                {
                    "trait_id": "facet_self_consciousness",
                    "name": "Self-consciousness",
                    "category": "personality",
                    "percentile": 0.1677698773671486,
                    "significant": true
                },
                {
                    "trait_id": "facet_vulnerability",
                    "name": "Susceptible to stress",
                    "category": "personality",
                    "percentile": 0.10426754062649501,
                    "significant": true
                }
            ]
        }
    ],
    "needs": [
        {
            "trait_id": "need_challenge",
            "name": "Challenge",
            "category": "needs",
            "percentile": 0.021334502895401286,
            "significant": true
        },
        {
            "trait_id": "need_closeness",
            "name": "Closeness",
            "category": "needs",
            "percentile": 0.47042825015389306,
            "significant": true
        },
        {
            "trait_id": "need_curiosity",
            "name": "Curiosity",
            "category": "needs",
            "percentile": 0.770458528156246,
            "significant": true
        },
        {
            "trait_id": "need_excitement",
            "name": "Excitement",
            "category": "needs",
            "percentile": 0.2016650912922372,
            "significant": true
        },
        {
            "trait_id": "need_harmony",
            "name": "Harmony",
            "category": "needs",
            "percentile": 0.42818273579054744,
            "significant": true
        },
        {
            "trait_id": "need_ideal",
            "name": "Ideal",
            "category": "needs",
            "percentile": 0.04332110778350229,
            "significant": true
        },
        {
            "trait_id": "need_liberty",
            "name": "Liberty",
            "category": "needs",
            "percentile": 0.10204964115850268,
            "significant": true
        },
        {
            "trait_id": "need_love",
            "name": "Love",
            "category": "needs",
            "percentile": 0.03221991374392019,
            "significant": true
        },
        {
            "trait_id": "need_practicality",
            "name": "Practicality",
            "category": "needs",
            "percentile": 0.020092255069610987,
            "significant": true
        },
        {
            "trait_id": "need_self_expression",
            "name": "Self-expression",
            "category": "needs",
            "percentile": 0.24567808535889002,
            "significant": true
        },
        {
            "trait_id": "need_stability",
            "name": "Stability",
            "category": "needs",
            "percentile": 0.4736586721005777,
            "significant": true
        },
        {
            "trait_id": "need_structure",
            "name": "Structure",
            "category": "needs",
            "percentile": 0.797651974666463,
            "significant": true
        }
    ],
    "values": [
        {
            "trait_id": "value_conservation",
            "name": "Conservation",
            "category": "values",
            "percentile": 0.4238712850681341,
            "significant": true
        },
        {
            "trait_id": "value_openness_to_change",
            "name": "Openness to change",
            "category": "values",
            "percentile": 0.7140145074119589,
            "significant": true
        },
        {
            "trait_id": "value_hedonism",
            "name": "Hedonism",
            "category": "values",
            "percentile": 0.03772086499626898,
            "significant": true
        },
        {
            "trait_id": "value_self_enhancement",
            "name": "Self-enhancement",
            "category": "values",
            "percentile": 0.007789918594954648,
            "significant": true
        },
        {
            "trait_id": "value_self_transcendence",
            "name": "Self-transcendence",
            "category": "values",
            "percentile": 0.36669998846156343,
            "significant": true
        }
    ],
    "warnings": []
}
```



**Analysis**:

- Helpful link: https://console.bluemix.net/docs/services/personality-insights/output.html#output

- Algorithm: transfer the JSON result to the different attributes of characteristics.

