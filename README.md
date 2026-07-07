# HOLOL POS — Station Windows (Café LM)

Application de station Windows pour le point de vente **HOLOL POS** (Café LM).
Ce dépôt sert **uniquement** à télécharger l'application. Aucun code source.

## Téléchargement

Télécharger le fichier depuis la dernière release :

➡️ **[HololPOS-CafeLM-Portable-1.0.0.exe](https://github.com/povssam/holol-pos-station-download/releases/latest)**

- Fichier : `HololPOS-CafeLM-Portable-1.0.0.exe`
- SHA256 : `4efc289140976de36a18a4e10ae33528f8721fa41a82d4655d341fc3b33d6167`

## Installation (station Windows Café LM)

1. **Télécharger** `HololPOS-CafeLM-Portable-1.0.0.exe`.
2. Le **poser sur le Bureau** de la station Windows Café LM.
3. **Double-cliquer** pour lancer l'application.
4. **SmartScreen** (si un avertissement Windows apparaît) :
   - Cliquer sur **Informations complémentaires**
   - Puis **Exécuter quand même**
5. **Pare-feu Windows** (si une fenêtre s'ouvre) : cliquer sur **Autoriser**.
6. **Se connecter** (Login).
7. Aller dans **Réglages → Imprimante**.
8. Vérifier que **Pont connecté** passe au **vert**. 🟢
9. Cliquer sur **Test Rongta brut**.

## Impression de test attendue

Le ticket imprimé doit afficher :

```
HOLOL TEST
CAFE LM
TEST IMPRESSION OK
```

Si le ticket sort correctement, la station est prête. ✅

## Vérifier le fichier (optionnel)

Sur la station Windows, dans PowerShell :

```powershell
Get-FileHash .\HololPOS-CafeLM-Portable-1.0.0.exe -Algorithm SHA256
```

La valeur doit correspondre au SHA256 ci-dessus.
