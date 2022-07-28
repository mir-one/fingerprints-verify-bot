# TON Fingerprints Verify
:gem: Verify DAO NFT Owners on The Open Network

## How bot works:

1. NFT holder writes a message to your bot
2. Bot sends the details for the transfer
3. Holder confirms ownership of the wallet
4. Bot sends a link to a private chat

## How to run bot
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/mir-one/fingerprints-verify-bot/tree/main)

### .env variables

You need to specify these env variables to run this bot. If you run it locally, you can also write them in `.env` text file.

``` bash
DATABASE_URL=       # PotsgreSQL database URL
BOT_TOKEN=          # Telegram bot API token from @BotFather // Example: 1234567890:ABCDEFGHIJKLMNOPQRSTUVWXYZ
COLLECTION=         # TON address of NFT collection. // Example: EQATbIOeT9ziq7Jf76dJlnWIAiZggY2TeDteAh46D4QICBZj
CHAT_ID=            # Telegram private chat for NFT owners. // Example: -10000000000
TONCENTER_API_KEY=  # toncenter.com API key from @tonapibot
HEROKU_APP_NAME=    # Name of your Heroku app for webhook setup (optional)
```
 
### Run bot locally

First, you need to install all dependencies:
  
```bash
pip install -r requirements.txt
```

Then you can run the bot. Don't forget to create `.env` file in the root folder with all required params (read above).

``` bash
python main.py
```

## Working with Database
If you want to add a user to the list of holders, but the collection has not yet reached the mint, you can add the necessary wallets to the **contest** table

Powered by [TON NFT Verificator Telegram bot](https://github.com/TON-Punks/ton-nft-verify-bot)