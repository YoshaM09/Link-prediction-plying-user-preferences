# Code for paper "Link prediction plying user preferences for mainstream, novelty, diversity and artistic similarities in music"

Link for dataset:

LFM-1b:
'http://www.cp.jku.at/datasets/LFM-1b/'

LFM-1b UGP:
'http://www.cp.jku.at/datasets/LFM-1b/'

LFM-1b social:
dataset link: https://zenodo.org/record/5585638

# Reproduce procedure

User_dataframe and Link_dataframe are generated using LFM-1b, LFM-1b UGP, LFM-1b social datasets.
LFM-1b_LEs.mat,LFM-1b_users_additional.txt are used from LFM-1b.
LFM-1b_UGP_weightedPC_allmusic.txt,LFM-1b_UGP_weightedPC_freebase.txt are used from LFM-1b UGP.
LFM-1b_users.txt,LFM-1b_social_ties.txt are used from LFM-1b social.

user_dfs contain users_df_no_missing_values.csv,users_df.csv.
link_dfs contain links_df_network_features.csv,links_df_demographic_features.csv,links_df_genre_features.csv,links_df_listening_profile_features.csv,links_df_listening_characteristics_features.csv

Similarity between the users based on Artist profile similarity and user groups M,N,D is calculated using users_df_no_missing_values.csv,links_df_full.csv.

For the link prediction experiment data from the above generated csv files are taken.
links_df_network_features.csv,links_df_listening_profile_features.csv,links_df_listening_characteristics_features.csv

Link prediction Experiment:

Baseline Approach
• The author intends to use the well-known algorithm
XGBoost to investigate merits of features M, N, and
D (MNDF) and user-artist profile features (APF) for
predicting link between the two nodes(users).
• Feature vector X is generated for link prediction and
is classified as (i)M, N, and D features (MNDF),(ii)
artist profile features (APF), and (iii) graph-based features
(GF), i.e. common neighbors.
• An 80/20 split is used to divide data into Train-Test
subsets and five fold cross validation is done.
• Link prediction accuracy result is measured with F1 score
for various combinations of features and compared with
a random classifier.

Proposed Approach
• A well-known algorithm
CatBoost to investigate merits of features M, N, and
D (MNDF) and user-artist profile features (APF) for
predicting link between the two nodes(users).
• Feature vector X is generated for link prediction and
is classified as (i)M, N, and D features (MNDF),(ii)
artist profile features (APF), and (iii) graph-based features
(GF), i.e. common neighbors.
• An 80/20 split is used to divide data into Train-Test
subsets and five fold cross validation is done.
• Link prediction accuracy result is measured with F1 score
for various combinations of features and compared with
a random classifier.

# References

paper link: https://arxiv.org/abs/2111.00562

@inproceedings{duricic2021my,
title={My friends also prefer diverse music: homophily and link prediction with user preferences for mainstream, novelty, and diversity in music},
author={Duricic, Tomislav and Kowald, Dominik and Schedl, Markus and Lex, Elisabeth},
booktitle={Proceedings of the 2021 IEEE/ACM International Conference on Advances in Social Networks Analysis and Mining},
pages={447--454},
year={2021}
}

paper link: https://dl.acm.org/doi/abs/10.1145/2911996.2912004

@inproceedings{schedl2016lfm,
title={The lfm-1b dataset for music retrieval and recommendation},
author={Schedl, Markus},
booktitle={Proceedings of the 2016 ACM on international conference on multimedia retrieval},
pages={103--110},
year={2016}
}

dataset link: https://zenodo.org/record/5585638

@dataset{tomislav_duricic_2021_5585638,
  author       = {Tomislav Duricic and
                  Dominik Kowald and
                  Markus Schedl and
                  Elisabeth Lex},
  title        = {Last.fm Social Connections},
  month        = oct,
  year         = 2021,
  publisher    = {Zenodo},
  doi          = {10.5281/zenodo.5585638},
  url          = {https://doi.org/10.5281/zenodo.5585638}
}


