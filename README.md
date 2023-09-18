# Navigating Out-of-Distribution Electricity Load Forecasting during COVID-19: A Continual Learning Approach Leveraging Human Mobility
![visual_abstract](/e18_vizabs.png)
This figure illustrates the impact of the first COVID-19 lockdown (indicated by the red region) on the electricity load of a building complex located in Melbourne’s Central Business District (top graph). Concurrently, it presents the effect on the average human mobility throughout the city, as measured by pedestrian count (bottom graph). The diagram clearly shows significant shifts in distributions during the lockdown, which do not fully revert to their pre-lockdown state even after restrictions are lifted

This is the official repo of the following paper: Navigating Out-of-Distribution Electricity Load Forecasting during COVID-19: A Continual Learning Approach Leveraging Human Mobility. In **BuildSys 2023**. https://arxiv.org/abs/2309.04296

This is a follow up paper on our previous work: Continually learning out-of-distribution spatiotemporal data for robust energy forecasting. In **ECML PKDD ADS 2023**. https://arxiv.org/abs/2306.06385 . [[Poster](/ECML_PKDD_energy_poster_v3.pdf)]

# Abstract

In traditional deep learning algorithms, one of the key assumptions is that the data distribution remains constant during both training and deployment. However, this assumption becomes problematic when faced with Out-of-Distribution periods, such as the COVID-19 lockdowns, where the data distribution significantly deviates from what the model has seen during training. This paper employs a two-fold strategy: utilizing continual learning techniques to update models with new data and harnessing human mobility data collected from privacy-preserving pedestrian counters located outside buildings. In contrast to online learning, which suffers from 'catastrophic forgetting' as newly acquired knowledge often erases prior information, continual learning offers a holistic approach by preserving past insights while integrating new data. This research applies FSNet, a powerful continual learning algorithm, to real-world data from 13 building complexes in Melbourne, Australia, a city which had the second longest total lockdown duration globally during the pandemic. Results underscore the crucial role of continual learning in accurate energy forecasting, particularly during Out-of-Distribution periods. Secondary data such as mobility and temperature provided ancillary support to the primary forecasting model. More importantly, while traditional methods struggled to adapt during lockdowns, models featuring at least online learning demonstrated resilience, with lockdown periods posing fewer challenges once armed with adaptive learning techniques. This study contributes valuable methodologies and insights to the ongoing effort to improve energy load forecasting during future Out-of-Distribution periods. 


# Results

This repo contains the complete results, while the paper only contains some selection of the results. This also includes perfomrnace during the training and validation sets, and as well as the standard deviations for all results.

The complete results is here: [Results_2_BuildSys23.csv](/Results_2_BuildSys23.csv). Note that `_u` is the mean while `_s` is the standard deviation. Some models are deterministic and do not have standard deviations.

If I have time, I might upload the hyperparameter and other stuff, like training time and memory use, as well.

Exponential smooting (`ES`) is not included as it is exactly the same as `CopyLastHour`.

# Data and Code

Unfortunately, the data and the code are private and cannot be published. This might change in the future. [Written on 2023 09 18]
