TP 3 : Lier Salle–Réservation–Utilisateur, ajouter Équipement (ManyToMany), expérimenter cascade et suppression orpheline
Dépendances JPA, Hibernate, Validator, H2, SLF4J et JUnit ajoutées.
-les etapes:

Configuration Java 1.8 ajoutée dans <properties>.

persistence.xml configuré avec H2 en mémoire et Hibernate.

Les 4 entités JPA ont été créées avec les relations suivantes :

Utilisateur ↔ Reservation : OneToMany / ManyToOne

Salle ↔ Reservation : OneToMany / ManyToOne

Salle ↔ Equipement : ManyToMany
Les méthodes utilitaires de gestion des relations bidirectionnelles ont été ajoutées.

La classe App contient les tests demandés :

cascade

suppression orpheline

relation ManyToMany
Note importante

J’ai ajouté aussi org.glassfish:javax.el dans le pom.xml. Cette dépendance est souvent nécessaire pour que hibernate-validator fonctionne correctement en exécution.

Je n’ai pas pu lancer mvn clean compile exec:java ici, car Maven n’est pas installé dans cet environnement.
-les resultats:
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-23 210336" src="https://github.com/user-attachments/assets/7057164a-6624-48a9-bbbc-0fa72efa5d4c" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-23 210353" src="https://github.com/user-attachments/assets/267d0995-c5db-4fa8-8cab-aa9d92f88a04" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-23 210402" src="https://github.com/user-attachments/assets/618ef36d-bec5-4506-a8d4-0234a2d7dbf3" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-23 210414" src="https://github.com/user-attachments/assets/d404ecdf-4fef-4170-8574-cf4460148489" />

<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-23 210424 - Copie (2)" src="https://github.com/user-attachments/assets/97b6dd38-2cae-4ae6-b8d3-c89c83e8ece7" />

<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-23 210518" src="https://github.com/user-attachments/assets/859383b0-ed4c-4754-848c-16b307aae5e2" />

<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-23 210526" src="https://github.com/user-attachments/assets/2d6b5972-4f78-4a47-8159-0e133e208c5d" />

<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-23 210533 - Copie (2)" src="https://github.com/user-attachments/assets/6b14883b-125a-4679-9c9d-fddf04e5e0c7" />


<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-23 210533" src="https://github.com/user-attachments/assets/154dec0a-b316-4e9c-9712-a82bd7ba7e5c" />
diagramme de classe
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 213918" src="https://github.com/user-attachments/assets/0d485e3f-9870-4d5f-9f6e-70c5b37ddd69" />
