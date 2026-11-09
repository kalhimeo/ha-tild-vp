These files are enhancements to the original CCEI integration here: https://github.com/developer-ccei-pool/home-assistant-vigipool-installer

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

I also share the code of my HA cards for editing programs. It requires the custom-features-card extension : https://github.com/Nerwyn/custom-card-features
I share you the code of the full dashboard page in the file ha-card-fullpage, here is how it looks :

<img width="837" height="516" alt="image" src="https://github.com/user-attachments/assets/08c0254e-afb5-47ec-9c3a-edbead9ea6d5" />

Do not hesitate to submit any improvements or fixes if you find bugs. Thanks!
