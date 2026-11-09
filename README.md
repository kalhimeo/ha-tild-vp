These files are enhancements to the original CCEI integration here: https://github.com/developer-ccei-pool/home-assistant-vigipool-installer

Among other things, they will let you do nice HA cards like those (see below) :

<img width="1623" height="1132" alt="image" src="https://github.com/user-attachments/assets/477e338c-11b0-4e22-b7f6-40995ac8f36d" />

<img width="842" height="530" alt="image" src="https://github.com/user-attachments/assets/3875b74d-5854-4750-bfb6-c47802b7237c" />

I only own the Tild VP, AnteaVS, Phileo VP, and Oxeo VP, so the enhancements in vigipool.yaml are only for those devices. You have to replace the XXXXXXXX in the code with your model ID.

Additionally, I vibe-coded 4 HA automations to decode and encode the programs for filtration and auxiliary (in my case, the auxiliary is the heat pump; maybe the frame differs for other types). You also need to edit the XXXXX at the end with the serial of your Tild VP and create the following helpers in HA :

  - input_boolean.tild_filtration_p1_thermoregule
  - input_select.tild_filtration_p1_vitesse
  - input_boolean.tild_filtration_p1_active
  - input_boolean.tild_filtration_p1_monday
  - input_boolean.tild_filtration_p1_tuesday
  - input_boolean.tild_filtration_p1_wednesday
  - input_boolean.tild_filtration_p1_thursday
  - input_boolean.tild_filtration_p1_friday
  - input_boolean.tild_filtration_p1_saturday
  - input_boolean.tild_filtration_p1_sunday
  - input_select.tild_filtration_p1_h1_debut
  - input_select.tild_filtration_p1_m1_debut
  - input_select.tild_filtration_p1_h1_fin
  - input_select.tild_filtration_p1_m1_fin
  - input_select.tild_filtration_p1_h2_debut
  - input_select.tild_filtration_p1_m2_debut
  - input_select.tild_filtration_p1_h2_fin
  - input_select.tild_filtration_p1_m2_fin
  - input_select.tild_filtration_p1_h3_debut
  - input_select.tild_filtration_p1_m3_debut
  - input_select.tild_filtration_p1_h3_fin
  - input_select.tild_filtration_p1_m3_fin
  - input_boolean.tild_filtration_p2_thermoregule
  - input_select.tild_filtration_p2_vitesse
  - input_boolean.tild_filtration_p2_active
  - input_boolean.tild_filtration_p2_monday
  - input_boolean.tild_filtration_p2_tuesday
  - input_boolean.tild_filtration_p2_wednesday
  - input_boolean.tild_filtration_p2_thursday
  - input_boolean.tild_filtration_p2_friday
  - input_boolean.tild_filtration_p2_saturday
  - input_boolean.tild_filtration_p2_sunday
  - input_select.tild_filtration_p2_h1_debut
  - input_select.tild_filtration_p2_m1_debut
  - input_select.tild_filtration_p2_h1_fin
  - input_select.tild_filtration_p2_m1_fin
  - input_select.tild_filtration_p2_h2_debut
  - input_select.tild_filtration_p2_m2_debut
  - input_select.tild_filtration_p2_h2_fin
  - input_select.tild_filtration_p2_m2_fin
  - input_select.tild_filtration_p2_h3_debut
  - input_select.tild_filtration_p2_m3_debut
  - input_select.tild_filtration_p2_h3_fin
  - input_select.tild_filtration_p2_m3_fin
  - input_boolean.tild_aux_p1_active
  - input_boolean.tild_aux_p1_monday
  - input_boolean.tild_aux_p1_tuesday
  - input_boolean.tild_aux_p1_wednesday
  - input_boolean.tild_aux_p1_thursday
  - input_boolean.tild_aux_p1_friday
  - input_boolean.tild_aux_p1_saturday
  - input_boolean.tild_aux_p1_sunday
  - input_select.tild_aux_p1_h1_debut
  - input_select.tild_aux_p1_m1_debut
  - input_select.tild_aux_p1_h1_fin
  - input_select.tild_aux_p1_m1_fin
  - input_select.tild_aux_p1_h2_debut
  - input_select.tild_aux_p1_m2_debut
  - input_select.tild_aux_p1_h2_fin
  - input_select.tild_aux_p1_m2_fin
  - input_select.tild_aux_p1_h3_debut
  - input_select.tild_aux_p1_m3_debut
  - input_select.tild_aux_p1_h3_fin
  - input_select.tild_aux_p1_m3_fin
  - input_boolean.tild_aux_p2_active
  - input_boolean.tild_aux_p2_monday
  - input_boolean.tild_aux_p2_tuesday
  - input_boolean.tild_aux_p2_wednesday
  - input_boolean.tild_aux_p2_thursday
  - input_boolean.tild_aux_p2_friday
  - input_boolean.tild_aux_p2_saturday
  - input_boolean.tild_aux_p2_sunday
  - input_select.tild_aux_p2_h1_debut
  - input_select.tild_aux_p2_m1_debut
  - input_select.tild_aux_p2_h1_fin
  - input_select.tild_aux_p2_m1_fin
  - input_select.tild_aux_p2_h2_debut
  - input_select.tild_aux_p2_m2_debut
  - input_select.tild_aux_p2_h2_fin
  - input_select.tild_aux_p2_m2_fin
  - input_select.tild_aux_p2_h3_debut
  - input_select.tild_aux_p2_m3_debut
  - input_select.tild_aux_p2_h3_fin
  - input_select.tild_aux_p2_m3_fin

Finally, you will also find the code of my different HA cards. These require additional Marketplace cards like custom-features-card (https://github.com/Nerwyn/custom-card-features), vertical-stack-in-card (https://github.com/ofekashery/vertical-stack-in-card) and statistics-graph-chart-card (https://github.com/cataseven/Statistics-Graph-Chart-Card).
There is one page with all the main pool cards, and a separate page with the program cards. I have put the code from the whole pages here for reference only. You may want to pick only the parts that interest you.

Do not hesitate to submit any improvements or fixes if you find bugs. Thanks!
