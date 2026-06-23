# Definitions & Taxonomy

## Columns

What each column on the RWA Dashboard represents.

### Identification & Naming

- **Ticker**: Canonical ticker symbol assigned to the asset or platform.
- **Name**: Human-readable name of the asset or platform.
- **Pair**: Trading pair as listed on the venue (e.g. `TSLA-USDT`, `OPENAI-USDC`).

### Links

- **Website**: Official website for the issuer, asset, or platform.
- **Twitter**: Official social account for the issuer, asset, or platform.
- **LinkedIn**: LinkedIn profile for the issuer or platform.
- **Discord**: Public Discord server invite.
- **Telegram**: Telegram channel or group.
- **Docs**: Documentation URL for the asset or platform.
- **Logo**: URL of the icon used on the dashboard.
- **GitHub**: GitHub organization or repo for the issuer, when public.

### Chains & Contracts

- **Primary Chain**: Primary blockchain used for the asset.
- **Chain**: All supported chains for the asset, if applicable.
- **Contracts**: Contract addresses for the asset across supported chains.

### Classification

- **Category**: High-level category grouping for the asset or platform.
- **Asset Class**: Specific asset class within the category.
- **Type**: Whether the row represents an Asset, Platform, or Wrapper.
- **RWA Classification**: High-level classification describing the economic nature of the entry.
- **Access Model**: Indicates how users interact with the asset (e.g. Permissionless, Permissioned).
- **Parent Platform**: Parent platform grouping when an asset is issued or managed under a broader platform.
- **Reference Asset**: The off-chain underlying the token or perp tracks.
- **Reference Asset Group**: High-level grouping of the reference asset (Public Equities, Bonds, ETFs, Stablecoin, etc.).
- **Settlement Asset / Margin Asset**: Asset used to margin and settle gains/losses on perpetual markets.

### Issuer & Regulatory

- **Issuer**: Legal issuer entity or responsible party.
- **Issuer Source Link**: Primary source link supporting issuer and product claims.
- **Issuer Registry Info**: Registry details for the issuer, including addresses, custodian notes, jurisdiction, and regulatory framework when applicable.
- **ISIN**: International Securities Identification Number, if applicable.

### Attestations & Risk

- **Attestation Links**: Links to proof-of-reserves, attestations, audits, or reserve reports.
- **Attestations**: Whether the asset has attestations.
- **Date of Last Attestation**: Date of the most recent published attestation.
- **Attestation Frequency**: Cadence of attestations (Daily, Monthly, Quarterly, Annual, On-demand, etc.).
- **Suspicious**: Whether the entry has been flagged for further review.

### Holder & Lifecycle

- **Redeemable**: Whether the asset can be redeemed for the underlying or a cash equivalent per documented terms.
- **Transferable**: Whether the token can be transferred onchain.
- **Self Custody**: Whether users can hold the token in a self-custody wallet.
- **Yield Bearing**: Whether the asset accrues yield to holders (via rebase, increasing balance, dividend, or NAV growth).
- **CEX Listed**: Whether the asset is available to trade on a centralized exchange.
- **KYC for mint/redeem**: Whether issuer minting and/or redemption requires identity verification.
- **KYC/Allowlisted/Whitelisted to Transfer/Hold**: Whether holding or transferring requires allowlisting or whitelisting.

### Oracles & Pricing (perps and synthetics)

- **Oracle Provider**: Price oracle used by the protocol or perp venue.
- **Oracle Proof Link**: Documentation URL describing the oracle methodology or feed sources.

### Notes

- **Description/Notes**: Summary of structure, backing, mechanics, and constraints.

## Type Taxonomy

Each entry on the RWA Dashboard is one of the following types.

- **Asset**: Primary token representing real-world asset exposure being tracked, not the platform enabling issuance, and not a wrapper of another tracked asset.
- **Platform**: Protocol, issuer, or infrastructure entry that enables issuance, custody, trading, or management of RWAs, but is not the RWA exposure token itself.
- **Wrapper**: Token that wraps, pools, tranches, or strategies one or more underlying assets, creating RWA exposure via a derivative or structured product.

## Category Taxonomy

Categories are the top-level grouping for assets and platforms on the dashboard. Each entry sits in one of the following.

- **Fiat Stablecoins**: Stablecoins designed to track a fiat currency, backed mainly by cash, deposits, and short-dated government securities.
- **RWA Stablecoins**: Fiat-pegged stablecoins whose primary backing is RWAs — commonly tokenized Treasuries, credit instruments, or other yield-bearing RWAs.
- **Non-RWA Stablecoins**: Stablecoins targeting a peg using onchain collateral or mechanisms rather than direct backing by real-world assets.
- **Bond & MMF Funds**: Tokens representing government debt instruments, bond exposure, money-market funds, or tokenized fund shares holding fixed-income assets.
- **Gold & Commodities**: Tokens representing commodity exposure, including precious metals, energy, industrial metals, and related baskets.
- **Real Estate**: Tokens representing real estate interests, fractional ownership, or revenue participation linked to property assets.
- **Stocks & Equities**: Tokens representing exposure to publicly traded equities, ETFs, indices, and private-equity / pre-IPO interests.
- **Other RWAs**: Tokens representing alternative assets that do not fit other categories, such as collectibles, IP / royalties, and exotic real assets.
- **Private Credit**: Tokens representing loans, receivables, invoices, structured credit, and other credit instruments backed by off-chain cashflows.
- **RWA Wrappers**: Tokens that wrap, pool, leverage, or strategize over one or more underlying RWA tokens or funds, creating composite RWA exposure.
- **Carbon & Environment**: Tokenized carbon credits and other environmental assets, including avoidance and removal instruments.
- **Governance Tokens**: Tokens used to govern RWA-related protocols. They do not represent direct claims on RWAs.
- **Crypto Funds**: Tokenized fund shares represented onchain providing managed exposure to crypto assets through a fund structure.
- **RWA Perps**: Perpetual futures markets and venues providing leveraged synthetic exposure to RWA reference prices (equities, ETFs, indices, commodities, bonds, real estate, FX, pre-IPO).

## Asset Class Taxonomy

Asset Class refines the Category by describing the specific token product structure (how the exposure is delivered onchain).

### Fiat Stablecoins

- **USD Stable**: Stablecoins pegged to USD and backed mainly by cash, bank deposits and short-term government paper held by a centralized issuer or custodian.
- **EUR Stable**: Stablecoins pegged to EUR and backed mainly by euro cash, bank deposits and short-term government paper.
- **Other Fiat Stable**: Stablecoins pegged to non-USD, non-EUR fiat currencies such as GBP, CHF, SGD or baskets of fiat.
- **Bank Deposit Token**: Tokens that represent a direct, redeemable claim on a bank or central bank deposit account at par value.
- **Yield Fiat Stable**: Fiat-pegged stablecoins that pass through some or all of the yield on reserve assets directly to token holders.

### RWA Stablecoins

- **RWA Fiat Stable**: Fiat-pegged stablecoins whose reserves are primarily real-world assets such as Treasury bills, bonds or commodity holdings (e.g. gold), but where yield is retained by the issuer rather than paid directly to token holders.
- **Yield RWA Stable**: Fiat-pegged stablecoins whose reserves are real-world asset portfolios and where yield is paid directly to token holders via an increasing balance or rebase.
- **Multi-Asset RWA Stable**: Stablecoins backed by a mix of real-world assets and onchain collateral, where neither side is clearly dominant.

### Non-RWA Stablecoins

- **Crypto Stable**: Stablecoins backed primarily by onchain crypto collateral (e.g. ETH, stETH, LP tokens) with no material allocation to real-world assets.
- **Algo Stable**: Stablecoins that rely mainly on algorithmic mechanisms or undercollateralized backing rather than fully reserved collateral.
- **Synthetic Stable**: Stablecoins backed by synthetic crypto or derivatives strategies (such as delta-neutral basis trades or perp hedging) rather than direct fiat or real-world asset reserves.

### Bond & MMF Funds

- **T-Bills**: Tokens that give direct or near-direct exposure to short-term government Treasury bills or ETFs that hold them.
- **Sovereign Bond Fund**: Tokenized vehicles that hold government notes and bonds with longer duration than T-bills.
- **Corp Bond Fund**: Tokenized funds that hold corporate bonds, securitized credit or similar corporate fixed-income instruments.
- **MMF**: Tokenized shares in a money market fund that holds short-duration, high-quality money market instruments.
- **Mixed RWA Fund**: Tokenized funds that hold a planned mix of sovereign debt, credit and cash-like assets where no single type dominates.

### Gold & Commodities

- **Gold**: Tokens backed by physical gold, whether allocated to specific bars or held in pooled, unallocated form by a custodian.
- **Silver**: Tokens backed primarily by physical silver held in secure custody.
- **Platinum**: Tokens backed primarily by physical platinum.
- **Palladium**: Tokens backed primarily by physical palladium.
- **Uranium**: Tokens backed primarily by uranium or uranium inventory.
- **Other Commodity**: Tokens backed by a single physical commodity that is not a precious metal or uranium, such as crude oil, natural gas, agricultural products, or metals outside the precious metals category.
- **Commodity Basket**: Tokens backed by a basket of commodities rather than a single underlying asset.
- **Commodity Backed**: Tokens 1:1 collateralized by physical commodity holdings.

### Real Estate

- **Single Property**: Tokens that give equity-style exposure to a single property or real estate project.
- **REIT**: Tokens that mirror units in a pooled real estate fund, REIT structure, or diversified basket/index of real estate exposures.
- **RE Revenue Share**: Tokens whose primary claim is to a share of rental income or other property revenue streams.
- **RE Credit**: Tokens backed primarily by loans to real estate projects or mortgages secured on property.

### Stocks & Equities

- **Synthetic Stock**: Tokens that track a single listed equity using synthetic replication rather than full custody of shares.
- **Stock Backed**: Tokens backed by held underlying shares in custody that map 1:1 to a single listed equity.
- **ETF Backed**: Tokens 1:1 collateralized by held shares of an exchange-traded fund, mapping one ETF unit to one token claim.
- **Equity Basket**: Tokens that track a basket or index of equities or equity ETFs.
- **PE / Venture**: Tokens that represent interests in private company equity, venture capital funds or similar vehicles.
- **Blockchain-Native Equity**: Tokens that constitute a listed equity natively on a blockchain as the canonical share registry rather than tokenizing off-chain custody.

### Other RWAs

- **Collectibles**: Tokens backed by art, collectibles, or other non-financial real assets such as luxury goods.
- **IP / Royalty**: Tokens whose primary claim is to intellectual property or revenue/royalties from IP such as music, patents or media catalogs.
- **Other Exotic**: Tokens backed by niche real-world assets that do not fit other categories, such as AI hardware, fleet assets or other specialized equipment.

### Private Credit

- **Credit Pool**: Pools or funds backed by diversified private loans such as SME, corporate or consumer credit, including managed private credit funds and feeder vehicles that allocate across lending strategies.
- **Trade Finance**: Pools backed by invoices, receivables or other trade-finance assets.
- **Structured Credit**: Credit backed by niche or structured assets such as revenue-based finance, litigation finance, project finance or asset-backed fleet financing.
- **Other Credit**: Private credit pools that are clearly real world lending exposures but do not fit the more specific labels.
- **Reinsurance Pool**: Pools where the primary risk and return come from reinsurance or insurance underwriting exposure.

### RWA Wrappers

- **Stable Yield Wrapper**: Wrappers whose underlying is one or more stablecoins and that issue a yield-bearing receipt token.
- **Single Asset Wrapper**: Wrappers that mainly hold one underlying RWA token or fund and issue a single receipt token.
- **RWA Basket Vault**: Wrappers that hold a basket of RWA tokens or funds and present them as one composite position or index-like exposure.
- **RWA LP Wrapper**: Tokens that represent LP positions where the majority of exposure is to RWA tokens or RWA stablecoins.
- **Leveraged RWA Vault**: Wrappers that apply leverage or active rebalancing on top of RWA collateral to modify yield or duration.
- **Structured Note**: Tokens that embed structured payouts or note-like features on top of underlying RWA collateral.
- **Yield Pool**: Tokens that directly represent a yield-generating RWA pool that is not positioned as a stablecoin.
- **Active Vault**: Vault tokens representing deposits into a discretionary, manager-directed strategy that may allocate across RWAs and other onchain yield sources, and that issue a receipt token.

### Carbon & Environment

- **Carbon Credit**: Tokens representing carbon credits, including project-based voluntary offsets and allowances from regulated cap-and-trade or compliance carbon markets.
- **Other Environmental**: Tokens linked to other environmental or impact units such as renewable energy certificates or biodiversity credits.
- **Carbon Reserve**: Tokens that function as reserve or treasury assets and are backed by baskets of carbon credits or similar environmental units, rather than representing individual retireable offset claims.

### Governance Tokens

- **Governance Token**: Tokens that confer governance rights, voting power or protocol control over an RWA platform or product suite, without being a direct 1:1 claim on the underlying assets.
- **Revenue Share**: Tokens that entitle holders to a share of protocol revenues or fees from an RWA platform while not being a direct claim on underlying asset pools.

### Crypto Funds

- **Crypto Index Fund**: Tokenized fund shares represented onchain that provide beneficial exposure to a diversified basket of cryptocurrencies via a disclosed index methodology or systematic allocation strategy. The onchain token represents the investor's economic interest in the fund under the applicable offering documents.
- **Crypto Hedge Fund**: Tokenized fund shares represented onchain that provide beneficial exposure to an actively managed digital-asset fund pursuing absolute-return strategies across spot and/or derivatives markets. The onchain token represents the investor's economic interest in the fund under the applicable offering documents.

### RWA Perps

- **Stock Perp**: Perpetual markets that track the price of an individual public company's equity. They provide margined, cash-settled equity exposure and do not confer ownership of the underlying shares.
- **ETF Perp**: Perpetual markets that track the price of an exchange-traded fund. They provide margined, cash-settled fund exposure and do not represent ownership of fund shares or redemption rights.
- **Equity Perp**: Perpetual markets that track a public-equity benchmark or basket. They provide margined, cash-settled index exposure rather than a directly backed token or ownership claim on constituent shares.
- **Equity Index Perp**: Perpetual markets that track a broad equity index: S&P 500, Nasdaq-100, Dow Jones, Nifty 50, Bovespa, or similar.
- **Commodity Perp**: Perpetual markets that track a commodity or commodity benchmark, such as gold or crude oil. They provide margined, cash-settled commodity exposure and do not represent title to physical inventory.
- **Bond Perp**: Perpetual markets that track a bond or bond benchmark, such as government bonds, bond ETFs, or fixed-income indices. They provide margined, cash-settled fixed-income exposure and do not represent ownership of the underlying securities.
- **Real Estate Perp**: Perpetual markets that track a real estate price index, such as a city or regional housing index. They provide margined, cash-settled real estate exposure and do not represent ownership of underlying property.
- **PE Perp**: Perpetual markets that track the estimated valuation of a private company. They provide margined, cash-settled exposure to private equity valuations and do not represent ownership of shares or partnership interests.
- **Forex Perps**: Perpetual markets that track a major or minor fiat currency pair (USDJPY, EURUSD, USDCAD, and similar).
- **Crypto Index Perp**: Perpetual markets that track a basket or index of crypto assets rather than a single coin.

## Asset Group Taxonomy

Asset Group describes the high-level grouping of the off-chain underlying that the token or perp tracks — distinct from Asset Class, which describes the token product structure.

- **Agricultural Commodities**: Assets tied mainly to crops, farmland yield rights, livestock-related commodity flows, or other agricultural commodity exposure.
- **AI & Compute Infrastructure**: Assets tied mainly to physical AI and compute infrastructure, such as GPUs, data centers, robotics equipment, tokenized compute capacity, or financing backed by those assets.
- **Bonds**: Assets tied mainly to government or corporate debt instruments, money market funds, or similar fixed-income exposures where returns come mainly from interest and principal payments.
- **Carbon Credits**: Assets tied mainly to carbon credits, emissions allowances, or other standardized environmental units used to represent avoided, reduced, or removed emissions.
- **Collectibles & Luxury Goods**: Assets tied mainly to art, watches, wine, jewelry, rare cars, luxury goods, or similar collectible markets.
- **Commodity Baskets**: Assets spanning multiple commodity types without one clearly dominant commodity.
- **Crypto / Digital Assets**: Assets tied mainly to cryptocurrencies, blockchain network activity, tokenized mining or hashrate, domain names, or investment funds whose reference assets are digital assets.
- **Energy**: Assets linked mainly to power generation, electricity, fuel infrastructure, or other energy-sector cash flows that are not best described as oil or natural gas alone.
- **Equity ETFs**: Assets whose primary reference is one or more exchange-traded funds that hold public equities.
- **Equity Indices**: Assets tracking broad or thematic equity indexes rather than a single company or a specific ETF.
- **Fiat Currencies**: Assets whose value is designed mainly to track a fiat currency or closely related cash unit, whether fully reserve-backed or maintained synthetically.
- **Industrial Metals**: Assets tied mainly to industrial metals such as copper, aluminum, nickel, or similar materials used in manufacturing and infrastructure.
- **Intellectual Property & Royalties**: Assets tied mainly to copyrights, music royalties, film rights, patents, trademarks, or other contractual cash flows from intellectual property.
- **Mixed Public Markets**: Assets spanning multiple public-market reference types, such as equities, ETFs, indices, bonds, or commodities, without one clearly dominant sleeve.
- **Multi-Asset RWAs**: Assets or platforms with meaningful exposure to multiple real-world asset sectors, such as bonds, credit, equities, real estate, or commodities, without one dominant reference asset.
- **Natural Gas**: Assets tied mainly to natural gas benchmarks or gas-linked commodity exposures.
- **Oil**: Assets tied mainly to crude oil benchmarks or related petroleum exposures.
- **Precious Metals**: Assets tied mainly to gold, silver, platinum, palladium, or similar precious-metals exposure.
- **Private Credit**: Assets tied mainly to privately originated loans, receivables, trade finance, structured credit, or similar non-public lending exposures.
- **Private Equity & Venture**: Assets tied mainly to ownership stakes in private companies, venture investments, or platform equity that behaves more like private-company exposure than public-market shares.
- **Public Equities**: Assets tied mainly to publicly listed companies or diversified baskets of listed shares.
- **Real Estate**: Assets linked mainly to property values, rental income, home equity, or portfolios of real estate assets.
- **Reinsurance**: Assets tied mainly to insurance-linked or reinsurance risk, where returns depend on underwriting performance, premium flows, and loss outcomes.
- **RWA Infrastructure**: Tokens or platforms tied mainly to the issuance, trading, settlement, compliance, or governance rails used to bring real-world assets onchain, rather than a single underlying asset class.
- **Commodities**: Assets tied mainly to commodities where the specific commodity is unclassified or spans multiple sub-types within commodities. Prefer more specific subtypes (Precious Metals, Industrial Metals, Energy, Oil, Natural Gas, Agricultural Commodities, Commodity Baskets) when possible.
- **Volatility**: Assets tied mainly to volatility indices such as the CBOE Volatility Index (VIX) or similar implied-volatility benchmarks.
- **Tax Credits**: Assets tied mainly to government tax credits or similar regulatory-based credits, such as production-based or investment-based tax incentives. Distinct from Carbon Credits.
