# mStable Process Diagrams

A repository of PlantUML diagrams that document the various mStable processes.

## mStable processes
* [Distribute Rewards](./distributions/README.md)
* [Liquidations](./liquidations/README.md)
* [Integrations](./integrations/README.md)
* [BuyBack & Make](./buyBack/README.md)

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
