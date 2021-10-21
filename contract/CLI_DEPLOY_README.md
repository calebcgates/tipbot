near delete tipbot.ninja.testnet ninja.testnet 

near create-account tipbot.ninja.testnet --masterAccount ninja.testnet

near deploy tipbot.ninja.testnet --wasmFile out/main.wasm \
  --initFunction 'new' \
  --initArgs '{"master_account_id": "ninja.testnet", "linkdrop_account_id":"linkdrop.ninja.testnet", "auth_account_id":"tipbotauth.ninja.testnet", "tiptoken_account_id":"tiptoken.ninja.testnet" }'
