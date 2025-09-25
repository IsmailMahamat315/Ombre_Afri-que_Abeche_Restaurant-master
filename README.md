# 🍽️ Ombre Afrique d’Abéché – Système de Gestion de Restaurant  

Solution de gestion pour un restaurant traditionnel à Abéché (Tchad), basée sur **MariaDB**.  
Elle couvre la gestion des **employés, commandes, factures, plats, stocks et réservations**.  

---

[Capture d’écran du 2025-07-07 11-20-45](https://github.com/user-attachments/assets/a27792fb-0ed8-4dc0-83fa-a7ebeb64bb45)![Capture d’écran du 2025-07-07 11-20-55](https://github.com/user-attachments/assets/a8f06a2e-bd49-48c0-9c85-74aadfb9ecc1)


## 🎯 Objectifs
- Digitaliser la prise de commande, la facturation et le suivi des stocks  
- Suivre ventes, paiements et réservations  
- Gérer employés et fournisseurs  
- Préparer des extensions futures (API, appli mobile, dashboard, etc.)  

---

## 🧩 Modélisation MERISE
- **Entités principales** : Employé, Plat, Commande, Facture, Ingrédient, Fournisseur, Réservation  
- **Relations clés** :  
  - Un employé → plusieurs commandes  
  - Une commande → une facture  
  - Un plat ↔ plusieurs ingrédients  
  - Un ingrédient ↔ plusieurs fournisseurs  

*(MCD, MLD, MPD et dictionnaire de données disponibles en schémas)*  

---

## 🗄️ Base de données (extrait)
| Table        | Rôle                              |
|--------------|-----------------------------------|
| `employe`    | Infos RH                          |
| `plat`       | Nom, prix, catégorie, ingrédients |
| `commande`   | Commandes clients                 |
| `facture`    | Paiements                         |
| `ingredient` | Stock                             |
| `fournisseur`| Sources produits                  |
| `reserver`   | Réservations                      |

---
### 1.Dicitionnaire de données

![Capture d’écran du 2025-07-07 12-11-13](https://github.com/user-attachments/assets/55d6aab4-9fe4-4730-83a6-5a79ec141d60)

![Capture d’écran du 2025-07-07 12-11-28](https://github.com/user-attachments/assets/c62b93c4-db4d-401e-9f19-09ddae83b462)

### 2. 🧩 MCD – Modèle Conceptuel de Données

![Capture d’écran du 2025-07-07 12-11-56](https://github.com/user-attachments/assets/5da63729-be0e-4db2-93f2-570974e635a1)

### 3. 🧩 MLD – Modèle Logique de Données

![Capture d’écran du 2025-07-07 12-11-42](https://github.com/user-attachments/assets/1096271f-2998-4e30-a2c6-2720aeeb1ec4)

### 4. 🧩 MPD – Modèle Physique de Données (Script SQL)

---

## 🧾 Données clés extraites

- **Nombre total d’employés** : 12
- ![Capture d’écran du 2025-07-07 13-53-45](https://github.com/user-attachments/assets/a769b0da-41c4-4255-9f53-e5de245c1987)

- **Total des factures analysées** : 11
- ![Capture d’écran du 2025-07-05 11-38-51](https://github.com/user-attachments/assets/9dff9be5-1a2b-462f-8595-5ad3a3db3f0a)

- **Modes de paiement** : espèces, carte bancaire, Mobile Money
- **Commandes** : sur place, à emporter, livraison
- ![Capture d’écran du 2025-07-07 13-57-11](https://github.com/user-attachments/assets/f3bcfcbc-cb93-4642-b5c7-75783157c4b4)

- **Plats disponibles** : 12 (recettes locales et modernes)
  ![Capture d’écran du 2025-07-07 14-00-05](https://github.com/user-attachments/assets/f8aed715-b66a-414a-a6be-afeef46528cb)

- **Ingrédients suivis en stock** : 12 types (mil, sorgho, viande, etc.)
  ![Capture d’écran du 2025-07-07 13-56-14](https://github.com/user-attachments/assets/e1ed9419-ef9d-456f-8d39-d15ff2be9706)

---
---


## 🔧 Technologies
- **MariaDB 10+**  
- **SQL**  
- **Modélisation UML / MERISE**  

---
---
## 🛠️ Étapes d’installation
### 1. 📁 Cloner le dépôt GitHub
```
     git clone https://github.com//Ombre_Afrique_Abeche_Restaurant.git
     cd Ombre_Afrique_Abeche_Restaurant
```
## 🗃️ Créer la base de données dans MariaDB
### 2.Connecte-toi à MariaDB :
```
sudo mariadb -u root -p

```
### 3.Crée la base de données :
```
CREATE DATABASE ombr_afrique_dabeche CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci;
EXIT;

```

