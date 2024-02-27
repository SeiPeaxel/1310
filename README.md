# snipea
Snipe NFTs on SEI.

# Features
1. Target a Collection on Pallet and ACQUIRE specific multiple NFTs that fall under a certain price point.
2. Target a Collection on Pallet and ACQUIRE any multiple NFTs that fall under a certain price point.
3. Target a Lighthouse Mint site and SECURE NFTs based on a mint limit per phase and mint limit overall total.

## Mint mode fees
MINT mode will incur a fee. If you do not hold at least 3 NFTs from my Peaxel Collection on SEI, you will be charged 0.1 SEI per successful mint.

You can purchase a Peaxel NFT from here: https://pallet.exchange/collection/peaxel

## Acquire mode fees
ACQUIRE mode is completely FREE to access and use for holders and non-holders of Peaxel NFTs.

# Installation
1. Install node js, npm, and git.
2. Clone this repo with git. In the terminal, run:
   ```bash
   git clone https://github.com/SeiPeaxel/1310
   ```
3. Navigate to the snipea directory. In the terminal, run:
   ```bash
   cd snipea
   ```
4. Install dependencies. In the terminal, run:
   ```bash
   npm install
   ```
5. In the snipea folder, create a ".env" file with the following settings. [An example file is included here.](https://github.com/fudgebucket27/snipea/blob/main/.env.example). 
   ```text
   RECOVERY_PHRASE=       your recovery phrase or private key; you can use multiple phrases or keys in MINT mode, just separate with commas.
   RPC_URL=               the SEI rpc url.
   MODE=                  set to ACQUIRE to snipe on pallet. Set to MINT to snipe Lighthouse mints.
   MINT_URL=              if using MINT mode, the url of the Lighthouse mint site, e.g., https://www.seitarded.xyz 
   MINT_LIMIT_PER_PHASE=  if using MINT mode, the amount of NFTs to mint per phase, e.g., 2
   MINT_LIMIT_PER_WALLET= if using MINT mode, the amount of NFTs to mint in total per wallet, e.g., 2 
   MINT_LIMIT_TOTAL=      if using MINT mode, the total number of NFTs to mint overall across all phases and wallets, e.g., 4 
   CONTRACT_ADDRESS=      if using ACQUIRE mode, the contract address for the collection on pallet, e.g., sei1e7mv93mrw629r66ykqc92gllls3dmsuytvetxzxpq8e5x6j3nj2qqjtxlr
   TOKEN_ID=              if using ACQUIRE mode, the token ID for the NFT; you can add multiple token IDs, just separate them with a comma or use SWEEP to search the first 25 NFTs in the collection that fall under the PRICE_LIMIT. Or use AUTO to keep acquiring 1 NFT at a time under the PRICE_LIMIT until the ACQUIRE_LIMIT is reached. 
   ACQUIRE_LIMIT=         if using SWEEP in TOKEN_ID, this is the number of NFTs to buy in a sweep in one transaction; limited to 25 max. If using AUTO, this is the max number of NFTs to acquire in total.
   PRICE_LIMIT=           if using ACQUIRE mode, it is the price limit to acquire the NFT, e.g., 0.3
   GAS_LIMIT=             the gas limit, e.g., 0.1
   POLLING_FREQUENCY=     in seconds, how often to check Pallet or the Mint UI site for listings/contract changes.
   ```

   For macOS and Linux, you may need to run this command in the terminal to create the ".env" file; you may need to show hidden items in the folder as well:
   ```bash
   touch .env
   ```
   
7. To run snipea, in the terminal, run:
   ```bash
   npm start run
   ```
