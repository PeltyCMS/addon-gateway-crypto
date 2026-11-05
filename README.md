# Crypto (Coinbase Commerce-style)

Official **PeltyCMS** `gateway` WASM addon (`gateway-crypto`).

## Install

1. Open Pelty Admin → Addons → Marketplace
2. Set registry URL to `https://market.mythicalsystems.org/api/pelty/addons/registry.json`
3. Download **Crypto (Coinbase Commerce-style)**

Marketplace: https://market.mythicalsystems.org/marketplace/product/gateway-crypto  
Product ID (CI): `48`

## Develop

This repository is a git submodule of [MythicalLTD/PeltyCMS](https://github.com/MythicalLTD/PeltyCMS) at `extensions/addons/crypto`.

```bash
# from the PeltyCMS monorepo
cargo xtask addons crypto
```

## Release (Mythic Marketplace)

Same flow as [featherpanel-com/PterodactylPanelApi](https://github.com/featherpanel-com/PterodactylPanelApi):

1. Repo secrets: `MYTHIC_PRODUCT_ID`, `MYTHIC_RELEASE_TOKEN`
2. Repo variable: `ADDON_DIR=crypto`
3. Actions → **Release Addon** → Run workflow

Publishes the packed `gateway-crypto.zip` via `MythicalLTD/.github/actions/publish-release@v1` and creates a GitHub Release.
