# HOLOL POS — Station Windows (Café LM)

Application de station Windows pour le point de vente **HOLOL POS** (Café LM).
Ce dépôt sert **uniquement** à télécharger l'application. Aucun code source.

## Téléchargement

Télécharger le fichier depuis la dernière release :

➡️ **[HololPOS-CafeLM-Portable-1.0.0.exe](https://github.com/povssam/holol-pos-station-download/releases/latest)**

- Fichier : `HololPOS-CafeLM-Portable-1.0.0.exe`
- SHA256 : `6ad3140aafc4d0b3a53d6f13d923a795d39372374688c4b9defa08a31babec4d`

## Installation (station Windows Café LM)

1. **Télécharger** `HololPOS-CafeLM-Portable-1.0.0.exe`.
2. Le **poser sur le Bureau** de la station Windows Café LM.
3. **Double-cliquer** pour lancer l'application.
4. **SmartScreen** (si un avertissement Windows apparaît) :
   - Cliquer sur **Informations complémentaires**
   - Puis **Exécuter quand même**
5. **Pare-feu Windows** (si une fenêtre s'ouvre) : cliquer sur **Autoriser**.
6. **Se connecter** (Login).
7. Aller dans **Plus → Imprimante**.
8. Choisir la **Rongta** dans la liste.
9. Cliquer sur **Test rapide Rongta**.

## Diagnostic (si un test échoue)

Dans **Plus → Imprimante**, cliquer sur **Diagnostic** pour ouvrir le Holol
Doctor. L'écran indique en haut **où est le problème** :

- **Problème matériel** : appuyer sur FEED sur la Rongta. Papier blanc = papier
  à l'envers ou tête thermique.
- **Problème Windows / driver** : lancer « Page test Windows ». Si Windows
  n'imprime pas, réinstaller le pilote Rongta.
- **Problème Holol RAW** : Windows imprime mais pas Holol. Vérifier l'imprimante
  sélectionnée et le spouleur.
- **Prêt** : le **Test Holol texte brut** imprime. La station est prête.

Lancer les tests dans l'ordre. Le premier qui doit passer est
**Test Holol texte brut**. En cas d'échec, utiliser **Copier rapport
diagnostic** ou **Copier erreur technique** et l'envoyer au support.

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
