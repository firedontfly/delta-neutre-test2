# delta-neutre-test2
bot un qui gere de façon automone une strategie de delta_neutre sur plusieur dexou cex
dex pris en charge : hyperliquid et paradex.
api hyperliquid : https://github.com/hyperliquid-dex/hyperliquid-python-sdk
api paradex : https://github.com/tradeparadex/paradex-py

liste et explication des fichier.

paradex_client.py
script que gere la liaison avec le dex paradex, il récupere les funding rates, le solde du compte, les ordres ouvert. il peut aussi ouvrir ou fermé des position long et short avec effet de levier.

hyperliquid_client.py
script que gere la liaison avec le dex hyperliquid, il récupere les funding rates, le solde du compte, les ordres ouvert. il peut aussi ouvrir ou fermé des position long et short avec effet de levier.

delta_neutre.py
script qui récupere les données fournie par les script client,il analyse les funding pour trouver les meilleurs paires de token entre dex. il verifie les solde des compte des dex, et determine la taille de la position a prendre. utilise les script client afin de lancer les ordres ou les fermer.

list_token.txt
liste des token pris en charge

.env
fichier environement dans lequel sont socker les clées et adresses
