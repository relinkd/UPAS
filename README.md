# UPAS

![User Public Achievement Logo](https://github.com/relinkd/UPAS/blob/main/images/upas_logo_x05_upd3.png)

## UPAS Components

1. [public-achievements](https://github.com/relinkd/public-achievements): Backend for Issuers
2. [UPAS_hub](https://github.com/relinkd/upas_hub): Frontend of UPAS hub
3. [UPAS_example](https://github.com/relinkd/upas_example_site): Example project site
4. [UPAS_marketplace](https://github.com/relinkd/upas_marketplace): Frontend and backend for marketplace

## Mainnet

**dapps**

[example_frontend](https://4zjqf-oyaaa-aaaal-qmzuq-cai.icp0.io)
[hub](https://4qk3z-yqaaa-aaaal-qmzva-cai.icp0.io)
[marketplace](https://46iwr-daaaa-aaaal-qmzua-cai.icp0.io)

**candides**

[example_backend](https://a4gq6-oaaaa-aaaab-qaa4q-cai.raw.icp0.io/?id=yb7fs-4qaaa-aaaal-qmzna-cai)
[icrc7](https://a4gq6-oaaaa-aaaab-qaa4q-cai.raw.icp0.io/?id=yuyu7-5yaaa-aaaal-qmzoq-cai)
[indexer](https://a4gq6-oaaaa-aaaab-qaa4q-cai.raw.icp0.io/?id=5tgs7-miaaa-aaaal-qmztq-cai)
[achievement](https://a4gq6-oaaaa-aaaab-qaa4q-cai.raw.icp0.io/?id=yg6dg-riaaa-aaaal-qmznq-cai)
[reputation_module](https://a4gq6-oaaaa-aaaab-qaa4q-cai.raw.icp0.io/?id=ytzsl-qaaaa-aaaal-qmzoa-cai)

## Deployment Instructions

1. Navigate to the `public-achievements` directory and run: `dfx deploy`
2. Deploy [yuku_icrc7](https://github.com/tuminfei/yuku_icrc7) and add the `reputation_module` canister ID as a minter: [icrc-7_configure.sh](https://github.com/relinkd/public-achievements/blob/main/test/icrc-7_configurate.sh) (your data)
3. Configure the reputation module with metadata, achievement canister ID, and yuku_icrc7 canister ID: [configure_upas.sh](https://github.com/relinkd/public-achievements/blob/main/test/configurate_upas.sh) (your_data)
4. Deploy the marketplace `dfx deploy`
5. Add your issuer to the indexer and verify as controller: [add_issuer.sh](https://github.com/relinkd/upas_marketplace/blob/main/test/add_issuer.sh) (your data)
6. Update the `UPAS_example` .env file with the following canister IDs:
- Indexer
- Reputation module
- Internet Identity
- Achievement
7. Update the `UPAS_Hub` .env file with the following canister IDs:
- Indexer
- Internet Identity

## Testing
After completing the deployment, you can test the system by attempting to receive an achievement and verifying it in the UPAS_Hub.

Note: Replace (your data) in sh files with the appropriate information for your deployment.