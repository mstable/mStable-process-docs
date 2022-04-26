# mStable Process Diagrams

A repository of PlantUML diagrams that document the various mStable processes.

## mStable Processes

Sequence diagrams of contract calls.

* [Distribute Rewards](./distributions/README.md)
* [Liquidations](./liquidations/README.md)
* [Governance Fees](./govFeeCollection/README.md)
* [Integrations](./integrations/README.md)
* [BuyBack & Make](./buyBack/README.md)
* [Emissions](./emissions/README.md)
* [Unwrapper](./unwrapper/README.md)

## Value (Token) Flows

Token transfers between contracts.

* [Token (Value) Flows](./valueFlows/README.md)

## Transaction Traces

[tx2uml](https://github.com/naddison36/tx2uml) traces of real transactions.

* [Save Wapper](./traces/README.md)
* [Staking V2](./stakingv2/README.md)

## PlantUML

[PlantUML](http://plantuml.com) is used for the technical diagrams using [Unified Modeling Language (UML)](https://en.wikipedia.org/wiki/Unified_Modeling_Language) and [Archimate](https://www.itmg-int.com/itmg-int-wp-content/Archimate/An%20Introduction%20to%20Archimate%203.0.pdf).

The PlantUML files have the `.puml` file extension.

To generate files, use the [node-plantuml](https://www.npmjs.com/package/node-plantuml) package installed globally.

```
npm i node-plantuml
```

```
cd liquidations
npx puml generate aaveFeedPoolLiquidator.puml -o aaveFeedPoolLiquidator.png
npx puml generate aaveMusdLiquidation.puml -o aaveMusdLiquidation.png
npx puml generate aaveMbtcLiquidation.puml -o aaveMbtcLiquidation.png
npx puml generate compLiquidation.puml -o compLiquidation.png
npx puml generate maticLiquidationPolygon.puml -o maticLiquidationPolygon.png

cd integrations
npx puml generate alchemixIntegration.puml -o alchemixIntegration.png
npx puml generate feederPoolIronBankIntegration.puml -o feederPoolIronBankIntegration.png

cd distributions
npx puml generate distributeRewardsMainnet.puml -o distributeRewardsMainnet.png
npx puml generate distributeRewardsPolygon.puml -o distributeRewardsPolygon.png
puml generate distributeRewardsMainnetAlchemix.puml -o distributeRewardsMainnetAlchemix.png

cd govFeeCollection
npx puml generate mainnetMusdFee.puml -o mainnetMusdFee.png
npx puml generate polygonMusdFee.puml -o polygonMusdFee.png

cd emissions
npx puml generate weeklyEmissions.puml -o weeklyEmissions.png
npx puml generate weeklyEmissions2TreasuryDAO.puml -o weeklyEmissions2TreasuryDAO.png
npx puml generate weeklyEmissions2Votium.puml -o weeklyEmissions2Votium.png
npx puml generate polygonBridge_frax.puml -o polygonBridge_frax.png
npx puml generate polygonBridge_vimUSD.puml -o polygonBridge_vimUSD.png
npx puml generate polygonBridge_balancer.puml -o polygonBridge_balancer.png
npx puml generate buyBackForStakers.puml -o buyBackForStakers.png

cd unwrapper
npx puml generate imusd_vault_bassets.puml -o imusd_vault_bassets.png
npx puml generate imusd_bassets.puml -o imusd_bassets.png
npx puml generate imusd_vault_busd.puml -o imusd_vault_busd.png
npx puml generate imusd_busd.puml -o imusd_busd.png

cd valueFlows
npx puml generate musdValueFlows.puml -o musdValueFlows.png
npx puml generate musdPolygonValueFlows.puml -o musdPolygonValueFlows.png
npx puml generate convexFlows.puml -o convexFlows.png
```

### VS Code extension

[Jebbs PlantUML](https://marketplace.visualstudio.com/items?itemName=jebbs.plantuml) extension for VS Code is used to authoring the PlantUML diagrams.

`Alt-D` on Windows, or `Option-D` on Mac, to start PlantUML preview in VS Code.

## Markdown table of contents

[markdown-toc](https://github.com/jonschlinkert/markdown-toc) can be used to generate a table of content for markdown files.

```
npm i markdown-toc
npx markdown-toc README.md --maxdepth 2
npx markdown-toc TokenSettlementProcesses.md --maxdepth 3
```

## Markdown to PDF conversion
To convert a markdown file to a pdf file, install [markdown-pdf](https://www.npmjs.com/package/markdown-pdf)

```
npm i markdown-pdf
```

The [custom-markdown-pdf.css](./custom-markdown-pdf.css) CSS file is required to prevent the urls from being displayed in the links.

Run the following to convert a markdown file to pdf
```
npx markdown-pdf AztecIntro.md -s custom-markdown-pdf.css
npx markdown-pdf TokenSettlementProcesses.md -s ./docs/custom-markdown-pdf.css
```

## Useful links

- [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
- [Plant UML Guide](http://plantuml.com/guide)
