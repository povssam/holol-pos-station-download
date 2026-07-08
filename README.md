# HOLOL POS — Station Windows (Café LM)

Application de station Windows pour le point de vente **HOLOL POS** (Café LM).
Ce dépôt sert **uniquement** à télécharger l'application. Aucun code source.

## ⬇️ Télécharger Windows Station

➡️ **[HololPOS-CafeLM-Portable-1.1.0.exe](https://github.com/povssam/holol-pos-station-download/releases/latest)**

- Fichier : `HololPOS-CafeLM-Portable-1.1.0.exe`
- SHA256 : `9a844f70dee2876f9597938b406ce78d2f38163602866831a4bf0a4be217a00b`

> L'installateur en un clic (`HololPOS-CafeLM-Setup-1.1.0.exe`, raccourcis Bureau +
> menu Démarrer, mise à jour auto) arrive prochainement. En attendant, la version
> portable ci-dessus est complète : téléchargez-la et lancez-la.

## Installation (station Windows Café LM)

1. **Télécharger** Windows Station (bouton ci-dessus).
2. **Lancer** le fichier `.exe`.
3. **SmartScreen** (si un avertissement apparaît) : **Informations complémentaires** → **Exécuter quand même**.
4. **Pare-feu** Windows : **Autoriser**.
5. Ouvrir **Holol POS Cafe LM** et se connecter.
6. Aller dans **Plus → Imprimante → Diagnostic**.
7. Lancer **Test Holol texte brut**.

## Impression de test attendue

```
HOLOL TEST
CAFE LM
TEST IMPRESSION OK
```

Si le ticket sort correctement, la station est prête. ✅

## Diagnostic (si un test échoue)

Dans **Plus → Imprimante → Diagnostic**, le haut de l'écran indique **où est le problème** :

- **Problème matériel** : appuyer sur FEED sur la Rongta. Papier blanc = papier à l'envers ou tête thermique.
- **Problème Windows / driver** : lancer « Page test Windows ». Si Windows n'imprime pas, réinstaller le pilote Rongta.
- **Problème Holol RAW** : Windows imprime mais pas Holol. Vérifier l'imprimante sélectionnée et le spouleur.
- **Prêt** : le **Test Holol texte brut** imprime. La station est prête.

En cas d'échec, utiliser **Copier rapport diagnostic** (ou **Copier erreur technique**)
et l'envoyer au support. Le journal est dans
`%APPDATA%\Holol POS Cafe LM\logs\bridge.log`.

## Vérifier le fichier (optionnel)

Sur la station Windows, dans PowerShell :

```powershell
Get-FileHash .\HololPOS-CafeLM-Portable-1.1.0.exe -Algorithm SHA256
```

La valeur doit correspondre au SHA256 ci-dessus.
