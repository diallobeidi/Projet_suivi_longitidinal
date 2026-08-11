ARCHITECTURE ENTITIES – PLATEFORME BOBOYE

1. 01_Boboye_Recensement_Entities.xlsx
   - Crée deux Entity Lists: menages_boboye et personnes_boboye.
   - Un ménage = une Entity menages_boboye.
   - Chaque membre du repeat = une Entity personnes_boboye.
   - Les propriétés sont reliées avec save_to et les préfixes menages_boboye# / personnes_boboye#.

2. 02_Boboye_Suivi_Personnes_Entities.xlsx
   - Utilise personnes_boboye.csv comme Entity List.
   - Sélectionne une personne existante.
   - Met à jour son statut, résidence, grossesse et certains indicateurs de suivi.

3. 03_Boboye_Grossesses_Entities.xlsx
   - Utilise personnes_boboye.csv pour sélectionner la femme.
   - Crée une Entity dans grossesses_boboye.
   - Enregistre CPN, issue de grossesse et accouchement.

IMPORTANT
- Les Entities doivent être créées/attachées dans ODK Central.
- Le champ select_one_from_file doit référencer le nom de l'Entity List, par exemple personnes_boboye.csv.
- Pour la mise à jour, la colonne entities.entity_id doit recevoir l'identifiant système de l'Entity sélectionnée.
- Les propriétés ID_MENAGE et ID_INDIVIDU sont des identifiants métier. Ils ne remplacent pas l'Entity system ID.
- Tester d'abord dans un projet ODK Central de test avec quelques ménages.
