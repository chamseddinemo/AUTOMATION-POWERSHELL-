# AUTOMATION-POWERSHELL-
AUTOMATION (POWERSHELL)

<h2>🟨 AUTOMATION (POWERSHELL)</h2>

<h2>🟨 PARTIE 3 — AUTOMATISATION ACTIVE DIRECTORY (POWERSHELL)</h2>

<h2>🎯 Objectif 📸</h2>

👉 📸 Screenshot conseillé : page titre du script / lab PowerShell en action

<p> assure dajouter LES PHOTOS : <img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Étapes de nettoyage du disque"/>  </p>

Automatiser la gestion d’Active Directory pour réduire les tâches manuelles, standardiser les comptes et appliquer des configurations à grande échelle.

---

<h2>1. 👤 CRÉATION AUTOMATIQUE DES UTILISATEURS</h2>

<h3>✔ Description 📸</h3>

👉 📸 Screenshot : script PowerShell + création user ADUC

Création massive d’utilisateurs dans Active Directory via script PowerShell.

<h3>✔ Étapes réalisées 📸</h3>

👉 📸 Screenshot : execution script + résultats users créés

Importation d’un fichier CSV contenant les utilisateurs  
Création automatique des comptes AD  
Attribution des paramètres :  
Nom complet  
SamAccountName  
UPN  
Mot de passe  
Activation du compte  

<h3>✔ Outils utilisés 📸</h3>

👉 📸 Screenshot : module AD PowerShell ou terminal

PowerShell  
ActiveDirectory module  
New-ADUser  
Import-Csv  

---

<h2>2. 📄 IMPORT CSV UTILISATEURS</h2>

<h3>✔ Description 📸</h3>

👉 📸 Screenshot : fichier CSV ouvert + import PowerShell

Utilisation d’un fichier CSV pour standardiser la création d’utilisateurs.

<h3>✔ Contenu CSV 📸</h3>

👉 📸 Screenshot : contenu CSV (Excel / Notepad)

FirstName  
LastName  
Username  
Password  
OU cible  

<h3>✔ Avantage 📸</h3>

👉 📸 Screenshot : batch users created

Gain de temps  
Réduction des erreurs humaines  
Création massive rapide  

---

<h2>3. 🏢 CRÉATION DES OUs (ORGANIZATIONAL UNITS)</h2>

<h3>✔ Description 📸</h3>

👉 📸 Screenshot : ADUC avec OU visibles

Création automatisée ou structurée des unités organisationnelles.

<h3>✔ OUs créées 📸</h3>

👉 📸 Screenshot : arborescence AD

OU_IT  
OU_HR  
OU_Finance  

<h3>✔ Rôle 📸</h3>

👉 📸 Screenshot : OU structure complète

Organisation logique de l’entreprise  
Application des GPO par département  
Gestion simplifiée des utilisateurs  

---

<h2>4. 👥 CRÉATION DES GROUPES AD</h2>

<h3>✔ Description 📸</h3>

👉 📸 Screenshot : création groupes AD

Création de groupes de sécurité pour gérer les permissions.

<h3>✔ Groupes créés 📸</h3>

👉 📸 Screenshot : liste groupes AD

GRP_IT  
GRP_HR  
GRP_FINANCE  

<h3>✔ Rôle 📸</h3>

👉 📸 Screenshot : groupe ouvert avec membres

Contrôle des accès  
Gestion des permissions  
Application des GPO  

---

<h2>5. 🔗 ATTRIBUTION UTILISATEURS → GROUPES</h2>

<h3>✔ Description 📸</h3>

👉 📸 Screenshot : user properties → member of tab

Les utilisateurs sont ajoutés aux groupes selon leur département.

<h3>✔ Exemple 📸</h3>

👉 📸 Screenshot : chaque user dans son groupe

Alex Perreira → GRP_IT  
Nina Belanger → GRP_HR  
Kevin Rimi → GRP_FINANCE  

<h3>✔ Avantage 📸</h3>

👉 📸 Screenshot : AD group membership

Gestion centralisée des droits  
Sécurité renforcée  

---

<h2>6. 🔗 LIAISON GROUPES ↔ OU (STRATÉGIE ENTREPRISE)</h2>

<h3>✔ Méthodes utilisées 📸</h3>

👉 📸 Screenshot : OU + group structure

Méthode 1 :  
Utilisateurs placés dans OU  
Groupes appliqués sur utilisateurs  

Méthode 2 :  
Groupes utilisés pour filtrage GPO  
OU utilisées pour organisation logique  

<h3>✔ Résultat 📸</h3>

👉 📸 Screenshot : AD structure complète

Contrôle double niveau :  
Organisation (OU)  
Sécurité (Groupes)  

---

<h2>7. 🔐 CRÉATION ET APPLICATION DES GPO</h2>

<h3>✔ Types de GPO créées 📸</h3>

👉 📸 Screenshot : GPMC console

---

<h3>🟦 GPO DOMAIN (GLOBAL)</h3>

👉 📸 Screenshot : domain GPO settings

Password policy  
Account lockout  
Audit security  

---

<h3>🟦 GPO IT (OU_IT)</h3>

👉 📸 Screenshot : GPO_IT linked to OU_IT

Blocage CMD / PowerShell  
Restriction panneau de configuration  
Outils admin uniquement  

---

<h3>🟦 GPO HR (OU_HR)</h3>

👉 📸 Screenshot : drive mapping + folder redirection

Drive mapping H:  
Redirection Documents/Desktop  
Blocage installation logiciels  

---

<h3>🟦 GPO FINANCE (OU_Finance)</h3>

👉 📸 Screenshot : USB restriction / drive X

Drive X: Finance  
Restriction USB  
Accès fichiers sensibles  

---

<h3>✔ Pourquoi appliquer chaque GPO 📸</h3>

👉 📸 Screenshot : comparaison policies

Domain GPO → sécurité globale entreprise  
IT GPO → protection environnements techniques  
HR GPO → simplicité utilisateur  
Finance GPO → protection données sensibles  

---

<h2>8. 🧪 TESTS ET VALIDATION</h2>

<h3>✔ Étapes de test 📸</h3>

👉 📸 Screenshot : gpresult /r output

Vérification création utilisateurs  
Test login domaine  
Vérification appartenance groupes  
Test accès fichiers  
Test application GPO (gpresult)  

<h3>✔ Outils utilisés 📸</h3>

👉 📸 Screenshot : terminal PowerShell + ADUC

gpresult /r  
Active Directory Users and Computers  
PowerShell Get-ADUser  

---

<h2>9. ⚙️ AUTRES AUTOMATISATIONS UTILISÉES EN ENTREPRISE</h2>

<h3>✔ 1. Reset password automatique 📸</h3>

👉 📸 Screenshot : Set-ADAccountPassword command  

---

<h3>✔ 2. Désactivation comptes inactifs 📸</h3>

👉 📸 Screenshot : disabled user in AD  

---

<h3>✔ 3. Audit utilisateurs 📸</h3>

👉 📸 Screenshot : export AD users CSV  

---

<h3>✔ 4. Gestion des licences 📸</h3>

👉 📸 Screenshot : M365 / Entra ID assignation  

---

<h3>✔ 5. Scripts de maintenance AD 📸</h3>

👉 📸 Screenshot : script cleanup AD  

---

<h2>💼 RÉSUMÉ DES COMPÉTENCES 📸</h2>

👉 📸 Screenshot final conseillé : lab complet AD + GPO  

✔ Automatisation AD  
Création massive utilisateurs  
Import CSV  
PowerShell scripting  

✔ Gestion entreprise  
OUs structurées  
Groupes de sécurité  
Permissions centralisées  

✔ Sécurité & GPO  
Policies domaine  
GPO par département  
Contrôle accès  

✔ Administration avancée  
Vérification AD  
Tests et validation  
Troubleshooting  

---

<h2>10. 🔐 GPO APPLIQUÉES DANS LE PROJET (DÉTAILLÉ COMPLET)</h2>

<h3>🎯 Objectif 📸</h3>

👉 📸 Screenshot : GPMC overview  

---

<h3>🟦 10.1 GPO AU NIVEAU DU DOMAINE (techcorp.local)</h3>

<h4>✔ Nom : GPO-Security-Baseline 📸</h4>

👉 📸 Screenshot : GPO settings  

<h4>✔ Appliqué sur 📸</h4>

👉 📸 Screenshot : domain link  

techcorp.local  

<h4>✔ Contenu 📸</h4>

👉 📸 Screenshot : password policy  

Password Policy  
Account Lockout Policy  
Audit logs  

---

<h3>🟩 10.2 GPO SUR GROUPES DE SÉCURITÉ</h3>

<h4>👨‍💻 GRP_IT 📸</h4>

👉 📸 Screenshot : IT GPO settings  

<h4>👩 GRP_HR 📸</h4>

👉 📸 Screenshot : HR drive mapping  

<h4>💰 GRP_FINANCE 📸</h4>

👉 📸 Screenshot : USB blocked / X drive  

---

<h3>🟨 10.3 GPO SUR ORGANIZATIONAL UNITS (OU)</h3>

<h4>🏢 OU_IT 📸</h4>

👉 📸 Screenshot : OU_IT GPO link  

<h4>🏢 OU_HR 📸</h4>

👉 📸 Screenshot : OU_HR GPO link  

<h4>🏢 OU_Finance 📸</h4>

👉 📸 Screenshot : OU_Finance GPO link  

---

<h3>🧪 10.5 TEST DES GPO</h3>

<h4>✔ Vérifications réalisées 📸</h4>

👉 📸 Screenshot : gpresult /r  

<h4>✔ Résultat 📸</h4>

👉 📸 Screenshot : final working policies  
