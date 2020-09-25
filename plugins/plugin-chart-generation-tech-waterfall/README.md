## @superset-ui/plugin-chart-generation-tech-waterfall

[![Version](https://img.shields.io/npm/v/@superset-ui/plugin-chart-generation-tech-waterfall.svg?style=flat-square)](https://img.shields.io/npm/v/@superset-ui/plugin-chart-generation-tech-waterfall.svg?style=flat-square)
[![David (path)](https://img.shields.io/david/apache-superset/superset-ui.svg?path=packages%2Fsuperset-ui-plugin-chart-generation-tech-waterfall&style=flat-square)](https://david-dm.org/apache-superset/superset-ui?path=packages/superset-ui-plugin-chart-generation-tech-waterfall)

This plugin provides Stacked waterfall chart for generation technology for Superset.

### Usage

Configure `key`, which can be any `string`, and register the plugin. This `key` will be used to lookup this chart throughout the app.

```js
import GenerationTechWaterfallChartPlugin from '@superset-ui/plugin-chart-generation-tech-waterfall';

new GenerationTechWaterfallChartPlugin()
  .configure({ key: 'generation-tech-waterfall' })
  .register();
```

Then use it via `SuperChart`. See [storybook](https://apache-superset.github.io/superset-ui/?selectedKind=plugin-chart-generation-tech-waterfall) for more details.

```js
<SuperChart
  chartType="generation-tech-waterfall"
  width={600}
  height={600}
  formData={...}
  queryData={{
    data: {...},
  }}
/>
```

### File structure generated

```
├── README.md
├── package.json
├── src
│   ├── GenerationTechWaterfall.tsx
│   ├── images
│   │   └── thumbnail.png
│   ├── index.ts
│   ├── plugin
│   │   ├── buildQuery.ts
│   │   ├── controlPanel.ts
│   │   ├── index.ts
│   │   └── transformProps.ts
│   └── types.ts
├── test
│   └── index.test.ts
└── types
    └── external.d.ts
```